---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeerasncontactdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
ms.openlocfilehash: f2bba3b69205585cd6d8f4834803a82bf15ec305
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063869"
---
# <span data-ttu-id="b78b1-101">New-AzPeerAsnContactDetail</span><span class="sxs-lookup"><span data-stu-id="b78b1-101">New-AzPeerAsnContactDetail</span></span>

## <span data-ttu-id="b78b1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b78b1-102">SYNOPSIS</span></span>
<span data-ttu-id="b78b1-103">Tworzy szczegółowe dane kontaktowe w pamięci dla PeerAsn.</span><span class="sxs-lookup"><span data-stu-id="b78b1-103">Creates an in memory contact detail for PeerAsn.</span></span> 

## <span data-ttu-id="b78b1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b78b1-104">SYNTAX</span></span>

```
New-AzPeerAsnContactDetail -Role <String> -Email <String> [-Phone <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b78b1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b78b1-105">DESCRIPTION</span></span>
<span data-ttu-id="b78b1-106">Utwórz w pamięci PeerAsn szczegóły kontaktu.</span><span class="sxs-lookup"><span data-stu-id="b78b1-106">Create an in memory PeerAsn contact detail.</span></span>

## <span data-ttu-id="b78b1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b78b1-107">EXAMPLES</span></span>

### <span data-ttu-id="b78b1-108">Tworzenie szczegółów kontaktu i dodawanie do PeerAsn</span><span class="sxs-lookup"><span data-stu-id="b78b1-108">Create contact detail and add to PeerAsn</span></span>
```powershell
PS C:\> $nocContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> $customerContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> New-AzPeerAsn -Name $name -PeerName "Contoso Networks Limited" -PeerAsn 65000 -ContactDetail $nocContact,$customerContact
```

<span data-ttu-id="b78b1-109">Rola i adres e-mail są wymagane.</span><span class="sxs-lookup"><span data-stu-id="b78b1-109">Role and email are required.</span></span> <span data-ttu-id="b78b1-110">Telefon jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="b78b1-110">Phone is optional.</span></span> <span data-ttu-id="b78b1-111">Telefon obsługuje znaki +-() lub spacje.</span><span class="sxs-lookup"><span data-stu-id="b78b1-111">Phone supports +-() or spaces.</span></span> <span data-ttu-id="b78b1-112">PeerAsn musi zawierać co najmniej jeden szczegół kontaktu typu "noc".</span><span class="sxs-lookup"><span data-stu-id="b78b1-112">A PeerAsn must include at least one contact detail of type "Noc"</span></span>

## <span data-ttu-id="b78b1-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b78b1-113">PARAMETERS</span></span>

### <span data-ttu-id="b78b1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b78b1-114">-DefaultProfile</span></span>
<span data-ttu-id="b78b1-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b78b1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b78b1-116">-Mail</span><span class="sxs-lookup"><span data-stu-id="b78b1-116">-Email</span></span>
<span data-ttu-id="b78b1-117">Adresy e-mail używane do kontaktowania się, jeśli problemy Arrise zwykle Network Operation Center</span><span class="sxs-lookup"><span data-stu-id="b78b1-117">Email Addresses used to contact if issues arrise typically a Network Operations Center</span></span>

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

### <span data-ttu-id="b78b1-118">-Phone</span><span class="sxs-lookup"><span data-stu-id="b78b1-118">-Phone</span></span>
<span data-ttu-id="b78b1-119">Telefon służący do kontaktowania się, gdy problemy Arrise zwykle sieciową usługą Operations Center</span><span class="sxs-lookup"><span data-stu-id="b78b1-119">Phone used to contact if issues arrise typically a Network Operations Center</span></span>

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

### <span data-ttu-id="b78b1-120">-Rola</span><span class="sxs-lookup"><span data-stu-id="b78b1-120">-Role</span></span>
<span data-ttu-id="b78b1-121">Wybierz rolę najlepiej pasującą do informacji kontaktowych.</span><span class="sxs-lookup"><span data-stu-id="b78b1-121">Choose the role that best suits the contact information.</span></span>
<span data-ttu-id="b78b1-122">Wymagany jest kontakt NOC.</span><span class="sxs-lookup"><span data-stu-id="b78b1-122">NOC Contact is required.</span></span>

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

### <span data-ttu-id="b78b1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b78b1-123">CommonParameters</span></span>
<span data-ttu-id="b78b1-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b78b1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b78b1-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b78b1-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b78b1-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b78b1-126">INPUTS</span></span>

### <span data-ttu-id="b78b1-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b78b1-127">None</span></span>

## <span data-ttu-id="b78b1-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b78b1-128">OUTPUTS</span></span>

### <span data-ttu-id="b78b1-129">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSContactDetail</span><span class="sxs-lookup"><span data-stu-id="b78b1-129">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail</span></span>

## <span data-ttu-id="b78b1-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b78b1-130">NOTES</span></span>

## <span data-ttu-id="b78b1-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b78b1-131">RELATED LINKS</span></span>
