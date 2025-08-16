# VRM 1.0 Technical Guide

*Note: The original document contains figures; this Markdown version includes summaries and key explanations. For full formatted content, see the PDF.*

---

## 1. What is VRM

VRM is a standard for handling humanoid 3D avatar data, also called the VRM format.  
It emphasizes cross-platform versatility, but initially, VRM 0.x (beta) was released in 2018 to gain early recognition. The official VRM 1.0 was released in 2022.  

VRM is widely used for applications such as the metaverse and Virtual YouTubers (VTubers).  
In Japan, platforms like **cluster** support VRM avatars.  
The **VRM Consortium** is the official organization maintaining the standard.  

Other 3D avatar formats exist (glTF, FBX, OBJ, COLLADA). VRM is specialized for humanoid characters, especially influenced by Japanese anime style, limiting recognition outside Japan. Collaboration with the KHRONOS Group aims to expand global adoption.

---

## 2. Current State of VRM 1.0

- Many users still use VRM 0.x and may mistakenly treat it as the standard.  
- Existing tools often do not fully support VRM 1.0, but VRM 0.x remains compatible, so creators tend to stick with it for stability.  
- **VRChat** does not natively support VRM, and VRM 1.0 features are difficult to reproduce; VRM 0.x is usually used as a source for conversion.  
- **cluster** now supports VRM 1.0, including constraints and inside colliders. However, many users rely on **VRoid Studio**, which simplifies avatar creation but does not expose advanced VRM 1.0 features. Blender or Unity is needed to fully utilize VRM 1.0.  

**Note:** VRoid Studio remains an intuitive, free tool that greatly supports VRM adoption.

---

## 3. Technical Factors Hindering Adoption

- **Backward compatibility issues:** VRM 1.0 may appear differently due to shader differences in VRM 0.x-optimized environments.  
- **Blend shapes redefined as Expressions** have caused confusion.  
- **Spring bones / secondary motion**: specifications changed significantly, complicating setup and affecting creators’ impressions.  
- **Survey by VRM Consortium (2023)**: most cited issues were spring bones, followed by materials (MToon10).  

Many issues could be mitigated with better documentation.  
- VRM specifications are fragmented and simplified, making it hard to judge whether avatar behavior is compliant.  
- Some rules (e.g., max 4 bones per vertex in skinning) require referencing **glTF 2.0**.  
- VRM 1.0 unique features are extensions not fully documented. Detailed explanations with practical examples are needed.  

**Examples:**  
- **Skirt collision prevention:** control spring chains with normal colliders (inside) and inside colliders (outside).  
- **Sleeve spring chains:** place a parent bone with an Aim constraint at the root; reference a bone parented to the Hips to orient the chain downwards.  
- **Rendering issues on cluster:** VRM 1.0 avatars may appear overly bright; VRM 0.x usually renders correctly.  

Constraints can make long sleeves of traditional Japanese clothing move naturally. Documentation should explain node constraints for reproducibility.

---

## 4. Conclusion

- VRM 1.0’s advantages are not obvious, and limited backward compatibility can make compliant avatars appear buggy.  
- **Developers** (e.g., UniVRM team) should provide guidance, warnings, and solutions.  
- **Users** should actively communicate questions and requests, even without deep specification knowledge.  
- Feedback shows **international interest** is high; providing content in English improves accessibility.  

---

## Download PDF

For full formatted content with figures:  
[VRM 1.0 Technical Guide PDF](./VRM1.0_Document_v1.pdf)

---

## License

*(Add your license here, e.g., MIT or Creative Commons)*
