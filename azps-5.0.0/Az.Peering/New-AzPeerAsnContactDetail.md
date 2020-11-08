---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeerasncontactdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
ms.openlocfilehash: f2bba3b69205585cd6d8f4834803a82bf15ec305
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225335"
---
# <span data-ttu-id="b709c-101">New-AzPeerAsnContactDetail</span><span class="sxs-lookup"><span data-stu-id="b709c-101">New-AzPeerAsnContactDetail</span></span>

## <span data-ttu-id="b709c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b709c-102">SYNOPSIS</span></span>
<span data-ttu-id="b709c-103">Tworzy szczegółowe dane kontaktowe w pamięci dla PeerAsn.</span><span class="sxs-lookup"><span data-stu-id="b709c-103">Creates an in memory contact detail for PeerAsn.</span></span> 

## <span data-ttu-id="b709c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b709c-104">SYNTAX</span></span>

```
New-AzPeerAsnContactDetail -Role <String> -Email <String> [-Phone <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b709c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b709c-105">DESCRIPTION</span></span>
<span data-ttu-id="b709c-106">Utwórz w pamięci PeerAsn szczegóły kontaktu.</span><span class="sxs-lookup"><span data-stu-id="b709c-106">Create an in memory PeerAsn contact detail.</span></span>

## <span data-ttu-id="b709c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b709c-107">EXAMPLES</span></span>

### <span data-ttu-id="b709c-108">Tworzenie szczegółów kontaktu i dodawanie do PeerAsn</span><span class="sxs-lookup"><span data-stu-id="b709c-108">Create contact detail and add to PeerAsn</span></span>
```powershell
PS C:\> $nocContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> $customerContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> New-AzPeerAsn -Name $name -PeerName "Contoso Networks Limited" -PeerAsn 65000 -ContactDetail $nocContact,$customerContact
```

<span data-ttu-id="b709c-109">Rola i adres e-mail są wymagane.</span><span class="sxs-lookup"><span data-stu-id="b709c-109">Role and email are required.</span></span> <span data-ttu-id="b709c-110">Telefon jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="b709c-110">Phone is optional.</span></span> <span data-ttu-id="b709c-111">Telefon obsługuje znaki +-() lub spacje.</span><span class="sxs-lookup"><span data-stu-id="b709c-111">Phone supports +-() or spaces.</span></span> <span data-ttu-id="b709c-112">PeerAsn musi zawierać co najmniej jeden szczegół kontaktu typu "noc".</span><span class="sxs-lookup"><span data-stu-id="b709c-112">A PeerAsn must include at least one contact detail of type "Noc"</span></span>

## <span data-ttu-id="b709c-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b709c-113">PARAMETERS</span></span>

### <span data-ttu-id="b709c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b709c-114">-DefaultProfile</span></span>
<span data-ttu-id="b709c-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b709c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b709c-116">-Mail</span><span class="sxs-lookup"><span data-stu-id="b709c-116">-Email</span></span>
<span data-ttu-id="b709c-117">Adresy e-mail używane do kontaktowania się, jeśli problemy Arrise zwykle Network Operation Center</span><span class="sxs-lookup"><span data-stu-id="b709c-117">Email Addresses used to contact if issues arrise typically a Network Operations Center</span></span>

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

### <span data-ttu-id="b709c-118">-Phone</span><span class="sxs-lookup"><span data-stu-id="b709c-118">-Phone</span></span>
<span data-ttu-id="b709c-119">Telefon służący do kontaktowania się, gdy problemy Arrise zwykle sieciową usługą Operations Center</span><span class="sxs-lookup"><span data-stu-id="b709c-119">Phone used to contact if issues arrise typically a Network Operations Center</span></span>

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

### <span data-ttu-id="b709c-120">-Rola</span><span class="sxs-lookup"><span data-stu-id="b709c-120">-Role</span></span>
<span data-ttu-id="b709c-121">Wybierz rolę najlepiej pasującą do informacji kontaktowych.</span><span class="sxs-lookup"><span data-stu-id="b709c-121">Choose the role that best suits the contact information.</span></span>
<span data-ttu-id="b709c-122">Wymagany jest kontakt NOC.</span><span class="sxs-lookup"><span data-stu-id="b709c-122">NOC Contact is required.</span></span>

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

### <span data-ttu-id="b709c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b709c-123">CommonParameters</span></span>
<span data-ttu-id="b709c-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b709c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b709c-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b709c-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b709c-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b709c-126">INPUTS</span></span>

### <span data-ttu-id="b709c-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b709c-127">None</span></span>

## <span data-ttu-id="b709c-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b709c-128">OUTPUTS</span></span>

### <span data-ttu-id="b709c-129">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSContactDetail</span><span class="sxs-lookup"><span data-stu-id="b709c-129">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail</span></span>

## <span data-ttu-id="b709c-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b709c-130">NOTES</span></span>

## <span data-ttu-id="b709c-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b709c-131">RELATED LINKS</span></span>
