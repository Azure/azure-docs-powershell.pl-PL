---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 77B26360-F22B-457F-BDE3-9920A5736947
online version: ''
schema: 2.0.0
ms.openlocfilehash: 323b04a57cffc71059dff3f91480d54684941695
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054637"
---
# <span data-ttu-id="4df66-101">Get-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="4df66-101">Get-AzureAffinityGroup</span></span>

## <span data-ttu-id="4df66-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4df66-102">SYNOPSIS</span></span>
<span data-ttu-id="4df66-103">Pobiera obiekt grupy koligacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4df66-103">Gets an Azure affinity group object.</span></span>

## <span data-ttu-id="4df66-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4df66-104">SYNTAX</span></span>

```
Get-AzureAffinityGroup [[-Name] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4df66-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4df66-105">DESCRIPTION</span></span>
<span data-ttu-id="4df66-106">Polecenie cmdlet **Get-AzureAffinityGroup** pobiera grupę koligacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4df66-106">The **Get-AzureAffinityGroup** cmdlet gets an Azure affinity group.</span></span>
<span data-ttu-id="4df66-107">Obiekt grupy koligacji zawiera nazwę grupy koligacji, lokalizację, etykietę, opis oraz magazyn i usługi hostowane, które są częścią grupy koligacji.</span><span class="sxs-lookup"><span data-stu-id="4df66-107">The affinity group object includes the affinity group name, location, label, description and the storage and hosted services that are part of the affinity group.</span></span>

## <span data-ttu-id="4df66-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4df66-108">EXAMPLES</span></span>

### <span data-ttu-id="4df66-109">Przykład 1: pobieranie właściwości grupy koligacji</span><span class="sxs-lookup"><span data-stu-id="4df66-109">Example 1: Get properties of an affinity group</span></span>
```
PS C:\> Get-AzureAffinityGroup -Name "South01"
```

<span data-ttu-id="4df66-110">To polecenie pobiera właściwości grupy koligacji o nazwie South01.</span><span class="sxs-lookup"><span data-stu-id="4df66-110">This command gets the properties of the affinity group named South01.</span></span>

## <span data-ttu-id="4df66-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4df66-111">PARAMETERS</span></span>

### <span data-ttu-id="4df66-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4df66-112">-InformationAction</span></span>
<span data-ttu-id="4df66-113">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="4df66-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4df66-114">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="4df66-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4df66-115">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="4df66-115">Continue</span></span>
- <span data-ttu-id="4df66-116">Ignorować</span><span class="sxs-lookup"><span data-stu-id="4df66-116">Ignore</span></span>
- <span data-ttu-id="4df66-117">Inquire</span><span class="sxs-lookup"><span data-stu-id="4df66-117">Inquire</span></span>
- <span data-ttu-id="4df66-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4df66-118">SilentlyContinue</span></span>
- <span data-ttu-id="4df66-119">Przestaw</span><span class="sxs-lookup"><span data-stu-id="4df66-119">Stop</span></span>
- <span data-ttu-id="4df66-120">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="4df66-120">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4df66-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4df66-121">-InformationVariable</span></span>
<span data-ttu-id="4df66-122">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="4df66-122">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4df66-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4df66-123">-Name</span></span>
<span data-ttu-id="4df66-124">Określa nazwę grupy koligacji, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4df66-124">Specifies the name of the affinity group that this cmdlet gets.</span></span>
<span data-ttu-id="4df66-125">Nazwy dla grup koligacji utworzonych za pośrednictwem portalu zarządzania są zazwyczaj identyfikatorami GUID.</span><span class="sxs-lookup"><span data-stu-id="4df66-125">Names for affinity groups created through the Management Portal are typically GUIDs.</span></span>
<span data-ttu-id="4df66-126">W porcie zarządzania jest wyświetlana etykieta grupy koligacji.</span><span class="sxs-lookup"><span data-stu-id="4df66-126">The Management Port shows the affinity group label.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4df66-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="4df66-127">-Profile</span></span>
<span data-ttu-id="4df66-128">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4df66-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4df66-129">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="4df66-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4df66-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4df66-130">CommonParameters</span></span>
<span data-ttu-id="4df66-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4df66-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4df66-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4df66-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4df66-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4df66-133">INPUTS</span></span>

## <span data-ttu-id="4df66-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4df66-134">OUTPUTS</span></span>

### <span data-ttu-id="4df66-135">AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="4df66-135">AffinityGroup</span></span>

## <span data-ttu-id="4df66-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4df66-136">NOTES</span></span>

## <span data-ttu-id="4df66-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4df66-137">RELATED LINKS</span></span>

[<span data-ttu-id="4df66-138">Nowe — AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="4df66-138">New-AzureAffinityGroup</span></span>](./New-AzureAffinityGroup.md)

[<span data-ttu-id="4df66-139">Remove-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="4df66-139">Remove-AzureAffinityGroup</span></span>](./Remove-AzureAffinityGroup.md)

[<span data-ttu-id="4df66-140">Set-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="4df66-140">Set-AzureAffinityGroup</span></span>](./Set-AzureAffinityGroup.md)


