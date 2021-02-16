---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeerasncontactdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
ms.openlocfilehash: f2bba3b69205585cd6d8f4834803a82bf15ec305
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184035"
---
# <span data-ttu-id="87026-101">New-AzPeerAsnContactDetail</span><span class="sxs-lookup"><span data-stu-id="87026-101">New-AzPeerAsnContactDetail</span></span>

## <span data-ttu-id="87026-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87026-102">SYNOPSIS</span></span>
<span data-ttu-id="87026-103">Tworzy szczegóły kontaktu w pamięci dla elementu równorzędnego.</span><span class="sxs-lookup"><span data-stu-id="87026-103">Creates an in memory contact detail for PeerAsn.</span></span> 

## <span data-ttu-id="87026-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="87026-104">SYNTAX</span></span>

```
New-AzPeerAsnContactDetail -Role <String> -Email <String> [-Phone <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87026-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="87026-105">DESCRIPTION</span></span>
<span data-ttu-id="87026-106">Utwórz szczegóły kontaktu równorzędnego w pamięci.</span><span class="sxs-lookup"><span data-stu-id="87026-106">Create an in memory PeerAsn contact detail.</span></span>

## <span data-ttu-id="87026-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="87026-107">EXAMPLES</span></span>

### <span data-ttu-id="87026-108">Tworzenie szczegółów kontaktu i dodawanie do komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="87026-108">Create contact detail and add to PeerAsn</span></span>
```powershell
PS C:\> $nocContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> $customerContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> New-AzPeerAsn -Name $name -PeerName "Contoso Networks Limited" -PeerAsn 65000 -ContactDetail $nocContact,$customerContact
```

<span data-ttu-id="87026-109">Rola i poczta e-mail są wymagane.</span><span class="sxs-lookup"><span data-stu-id="87026-109">Role and email are required.</span></span> <span data-ttu-id="87026-110">Telefon jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="87026-110">Phone is optional.</span></span> <span data-ttu-id="87026-111">Telefon obsługuje klawisze +-() lub spacje.</span><span class="sxs-lookup"><span data-stu-id="87026-111">Phone supports +-() or spaces.</span></span> <span data-ttu-id="87026-112">PeerAsn musi zawierać co najmniej jeden szczegół kontaktu typu "Noc"</span><span class="sxs-lookup"><span data-stu-id="87026-112">A PeerAsn must include at least one contact detail of type "Noc"</span></span>

## <span data-ttu-id="87026-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87026-113">PARAMETERS</span></span>

### <span data-ttu-id="87026-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87026-114">-DefaultProfile</span></span>
<span data-ttu-id="87026-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="87026-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87026-116">— Poczta e-mail</span><span class="sxs-lookup"><span data-stu-id="87026-116">-Email</span></span>
<span data-ttu-id="87026-117">Adresy e-mail używane do kontaktowania się w przypadku powstania problemów zazwyczaj z Centrum operacji sieciowych</span><span class="sxs-lookup"><span data-stu-id="87026-117">Email Addresses used to contact if issues arrise typically a Network Operations Center</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87026-118">— Telefon</span><span class="sxs-lookup"><span data-stu-id="87026-118">-Phone</span></span>
<span data-ttu-id="87026-119">Telefon używany do kontaktowania się w przypadku problemów z centrum operacji sieciowych</span><span class="sxs-lookup"><span data-stu-id="87026-119">Phone used to contact if issues arrise typically a Network Operations Center</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87026-120">— Rola</span><span class="sxs-lookup"><span data-stu-id="87026-120">-Role</span></span>
<span data-ttu-id="87026-121">Wybierz rolę, która najlepiej pasuje do informacji kontaktowych.</span><span class="sxs-lookup"><span data-stu-id="87026-121">Choose the role that best suits the contact information.</span></span>
<span data-ttu-id="87026-122">Kontakt NOC jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="87026-122">NOC Contact is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87026-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87026-123">CommonParameters</span></span>
<span data-ttu-id="87026-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87026-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87026-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="87026-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87026-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87026-126">INPUTS</span></span>

### <span data-ttu-id="87026-127">Brak</span><span class="sxs-lookup"><span data-stu-id="87026-127">None</span></span>

## <span data-ttu-id="87026-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="87026-128">OUTPUTS</span></span>

### <span data-ttu-id="87026-129">Microsoft.Azure.PowerShell.Cmdlet.Peering.Models.PSContactDetail</span><span class="sxs-lookup"><span data-stu-id="87026-129">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail</span></span>

## <span data-ttu-id="87026-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="87026-130">NOTES</span></span>

## <span data-ttu-id="87026-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="87026-131">RELATED LINKS</span></span>
