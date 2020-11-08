---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B2C7E454-F38F-4139-ADA2-D1C59C03CC50
online version: ''
schema: 2.0.0
ms.openlocfilehash: efa519c380ffa78f44e8ac6edebda284a4ce3cd0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055397"
---
# <span data-ttu-id="11865-101">Set-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="11865-101">Set-AzureAffinityGroup</span></span>

## <span data-ttu-id="11865-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="11865-102">SYNOPSIS</span></span>
<span data-ttu-id="11865-103">Modyfikuje właściwości grupy koligacji.</span><span class="sxs-lookup"><span data-stu-id="11865-103">Modifies properties of an affinity group.</span></span>

## <span data-ttu-id="11865-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="11865-104">SYNTAX</span></span>

```
Set-AzureAffinityGroup [-Name] <String> -Label <String> [-Description <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="11865-105">Opis</span><span class="sxs-lookup"><span data-stu-id="11865-105">DESCRIPTION</span></span>
<span data-ttu-id="11865-106">Polecenie cmdlet **Set-AzureAffinityGroup** modyfikuje właściwości grupy koligacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="11865-106">The **Set-AzureAffinityGroup** cmdlet modifies properties of an Azure affinity group.</span></span>
<span data-ttu-id="11865-107">Możesz zmienić etykietę i opis.</span><span class="sxs-lookup"><span data-stu-id="11865-107">You can change the label and the description.</span></span>

## <span data-ttu-id="11865-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="11865-108">EXAMPLES</span></span>

### <span data-ttu-id="11865-109">Przykład 1. Modyfikowanie grupy koligacji</span><span class="sxs-lookup"><span data-stu-id="11865-109">Example 1: Modify an affinity group</span></span>
```
PS C:\> Set-AzureAffinityGroup -Name "South01" -Label "SouthUSProduction" -Description "Production applications for Southern US locations"
```

<span data-ttu-id="11865-110">To polecenie modyfikuje etykietę grupy koligacji o nazwie South01, która ma zostać SouthUSProduction, a polecenie modyfikuje również opis.</span><span class="sxs-lookup"><span data-stu-id="11865-110">This command modifies the label of the affinity group named South01 to be SouthUSProduction The command also modifies the description.</span></span>

## <span data-ttu-id="11865-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="11865-111">PARAMETERS</span></span>

### <span data-ttu-id="11865-112">— Opis</span><span class="sxs-lookup"><span data-stu-id="11865-112">-Description</span></span>
<span data-ttu-id="11865-113">Umożliwia określenie opisu grupy koligacji.</span><span class="sxs-lookup"><span data-stu-id="11865-113">Specifies the description of the affinity group.</span></span>
<span data-ttu-id="11865-114">Długość opisu może wynosić do 1024 znaków.</span><span class="sxs-lookup"><span data-stu-id="11865-114">The description can be up to 1024 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11865-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="11865-115">-InformationAction</span></span>
<span data-ttu-id="11865-116">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="11865-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="11865-117">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="11865-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="11865-118">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="11865-118">Continue</span></span>
- <span data-ttu-id="11865-119">Ignorować</span><span class="sxs-lookup"><span data-stu-id="11865-119">Ignore</span></span>
- <span data-ttu-id="11865-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="11865-120">Inquire</span></span>
- <span data-ttu-id="11865-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="11865-121">SilentlyContinue</span></span>
- <span data-ttu-id="11865-122">Przestaw</span><span class="sxs-lookup"><span data-stu-id="11865-122">Stop</span></span>
- <span data-ttu-id="11865-123">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="11865-123">Suspend</span></span>

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

### <span data-ttu-id="11865-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="11865-124">-InformationVariable</span></span>
<span data-ttu-id="11865-125">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="11865-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="11865-126">-Label</span><span class="sxs-lookup"><span data-stu-id="11865-126">-Label</span></span>
<span data-ttu-id="11865-127">Określa etykietę grupy koligacji.</span><span class="sxs-lookup"><span data-stu-id="11865-127">Specifies a label for the affinity group.</span></span>
<span data-ttu-id="11865-128">Etykieta może mieć długość do 100 znaków.</span><span class="sxs-lookup"><span data-stu-id="11865-128">The label can be up to 100 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11865-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="11865-129">-Name</span></span>
<span data-ttu-id="11865-130">Określa nazwę grupy koligacji, którą to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="11865-130">Specifies the name of the affinity group that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11865-131">-Profile</span><span class="sxs-lookup"><span data-stu-id="11865-131">-Profile</span></span>
<span data-ttu-id="11865-132">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11865-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="11865-133">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="11865-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="11865-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11865-134">CommonParameters</span></span>
<span data-ttu-id="11865-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11865-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11865-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11865-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11865-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11865-137">INPUTS</span></span>

## <span data-ttu-id="11865-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="11865-138">OUTPUTS</span></span>

## <span data-ttu-id="11865-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="11865-139">NOTES</span></span>

## <span data-ttu-id="11865-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="11865-140">RELATED LINKS</span></span>

[<span data-ttu-id="11865-141">Get-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="11865-141">Get-AzureAffinityGroup</span></span>](./Get-AzureAffinityGroup.md)

[<span data-ttu-id="11865-142">Nowe — AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="11865-142">New-AzureAffinityGroup</span></span>](./New-AzureAffinityGroup.md)

[<span data-ttu-id="11865-143">Remove-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="11865-143">Remove-AzureAffinityGroup</span></span>](./Remove-AzureAffinityGroup.md)


