Voeg een collider toe aan het GameObject die moet reageren op een botsing en schakel 'Is Trigger' in de Inspector in.

![Collider component met 'is Trigger' aangevinkt.](images/collider-trigger.png)

Zorg ervoor dat het GameObject dat ermee in botsing komt ook een collider heeft.

Voeg `OnTriggerEnter` en/of `OnTriggerExit` methoden toe aan het GameObject met 'Is Trigger' ingeschakeld.

--- code ---
---
language: csharp
filename: 
line_numbers: false
line_number_start: 
line_highlights: 
---
    void OnTriggerEnter(Collider other)
    {
        if(other.gameObject.tag == "Player")
        {
            Debug.Log("Speler is aangekomen");
        }
    }
    
    void OnTriggerExit(Collider other)
    {
        if(other.gameObject.tag == "Player")
        {
            Debug.Log("Speler is vertrokken");
        }
    }
--- /code ---

**Foutopsporing:** Vergeet niet om 'Is trigger' in te schakelen en ervoor te zorgen dat beide GameObjects een collider hebben. 
