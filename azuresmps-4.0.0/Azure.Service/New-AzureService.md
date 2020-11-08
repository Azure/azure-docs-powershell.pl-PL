---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BB216903-B2BB-4948-AC28-408ED6C768F2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6cae249f99282006ff8636e8d727485a223e2a1d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054865"
---
# <span data-ttu-id="38dfa-101">New-AzureService</span><span class="sxs-lookup"><span data-stu-id="38dfa-101">New-AzureService</span></span>

## <span data-ttu-id="38dfa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="38dfa-102">SYNOPSIS</span></span>
<span data-ttu-id="38dfa-103">Tworzy usługę Azure.</span><span class="sxs-lookup"><span data-stu-id="38dfa-103">Creates an Azure service.</span></span>

## <span data-ttu-id="38dfa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="38dfa-104">SYNTAX</span></span>

### <span data-ttu-id="38dfa-105">ParameterSetAffinityGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="38dfa-105">ParameterSetAffinityGroup (Default)</span></span>
```
New-AzureService [-ServiceName] <String> [-AffinityGroup] <String> [[-Label] <String>]
 [[-Description] <String>] [[-ReverseDnsFqdn] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="38dfa-106">ParameterSetLocation</span><span class="sxs-lookup"><span data-stu-id="38dfa-106">ParameterSetLocation</span></span>
```
New-AzureService [-ServiceName] <String> [-Location] <String> [[-Label] <String>] [[-Description] <String>]
 [[-ReverseDnsFqdn] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="38dfa-107">Opis</span><span class="sxs-lookup"><span data-stu-id="38dfa-107">DESCRIPTION</span></span>
<span data-ttu-id="38dfa-108">Polecenie cmdlet **New-AzureService** tworzy nową usługę Azure w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="38dfa-108">The **New-AzureService** cmdlet creates a new Azure service in the current subscription.</span></span>

## <span data-ttu-id="38dfa-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="38dfa-109">EXAMPLES</span></span>

### <span data-ttu-id="38dfa-110">Przykład 1. Tworzenie usługi</span><span class="sxs-lookup"><span data-stu-id="38dfa-110">Example 1: Create a service</span></span>
```
PS C:\> New-AzureService -ServiceName "MySvc01" -Label "MyTestService" -Location "South Central US"
```

<span data-ttu-id="38dfa-111">To polecenie tworzy nową usługę o nazwie MySvc01 w amerykańskiej lokalizacji Stanów Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="38dfa-111">This command creates a new service named MySvc01 in the South Central US location.</span></span>

### <span data-ttu-id="38dfa-112">Przykład 2: Tworzenie usługi w grupie koligacji</span><span class="sxs-lookup"><span data-stu-id="38dfa-112">Example 2: Create a service in an affinity group</span></span>
```
PS C:\> New-AzureService -ServiceName "MySvc01" -AffinityGroup NorthRegion
```

<span data-ttu-id="38dfa-113">To polecenie tworzy nową usługę o nazwie MySvc01 przy użyciu grupy koligacji NorthRegion.</span><span class="sxs-lookup"><span data-stu-id="38dfa-113">This command creates a new service named MySvc01 using the NorthRegion affinity group.</span></span>

## <span data-ttu-id="38dfa-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="38dfa-114">PARAMETERS</span></span>

### <span data-ttu-id="38dfa-115">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="38dfa-115">-AffinityGroup</span></span>
<span data-ttu-id="38dfa-116">Określa grupę koligacji skojarzoną z subskrypcją.</span><span class="sxs-lookup"><span data-stu-id="38dfa-116">Specifies the affinity group associated with the subscription.</span></span>
<span data-ttu-id="38dfa-117">Jeśli nie określono parametru *Location* , wymagana jest grupa koligacji.</span><span class="sxs-lookup"><span data-stu-id="38dfa-117">If you do not specify the *Location* parameter, an affinity group is required.</span></span>

```yaml
Type: String
Parameter Sets: ParameterSetAffinityGroup
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38dfa-118">— Opis</span><span class="sxs-lookup"><span data-stu-id="38dfa-118">-Description</span></span>
<span data-ttu-id="38dfa-119">Określa opis usługi.</span><span class="sxs-lookup"><span data-stu-id="38dfa-119">Specifies a description for the service.</span></span>
<span data-ttu-id="38dfa-120">Długość opisu może wynosić do 1024 znaków.</span><span class="sxs-lookup"><span data-stu-id="38dfa-120">The description may be up to 1024 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38dfa-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="38dfa-121">-InformationAction</span></span>
<span data-ttu-id="38dfa-122">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="38dfa-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="38dfa-123">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="38dfa-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="38dfa-124">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="38dfa-124">Continue</span></span>
- <span data-ttu-id="38dfa-125">Ignorować</span><span class="sxs-lookup"><span data-stu-id="38dfa-125">Ignore</span></span>
- <span data-ttu-id="38dfa-126">Inquire</span><span class="sxs-lookup"><span data-stu-id="38dfa-126">Inquire</span></span>
- <span data-ttu-id="38dfa-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="38dfa-127">SilentlyContinue</span></span>
- <span data-ttu-id="38dfa-128">Przestaw</span><span class="sxs-lookup"><span data-stu-id="38dfa-128">Stop</span></span>
- <span data-ttu-id="38dfa-129">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="38dfa-129">Suspend</span></span>

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

### <span data-ttu-id="38dfa-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="38dfa-130">-InformationVariable</span></span>
<span data-ttu-id="38dfa-131">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="38dfa-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="38dfa-132">-Label</span><span class="sxs-lookup"><span data-stu-id="38dfa-132">-Label</span></span>
<span data-ttu-id="38dfa-133">Określa etykietę usługi.</span><span class="sxs-lookup"><span data-stu-id="38dfa-133">Specifies a label for the service.</span></span>
<span data-ttu-id="38dfa-134">Etykieta może mieć długość do 100 znaków.</span><span class="sxs-lookup"><span data-stu-id="38dfa-134">The label may be up to 100 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38dfa-135">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="38dfa-135">-Location</span></span>
<span data-ttu-id="38dfa-136">Określa lokalizację usługi.</span><span class="sxs-lookup"><span data-stu-id="38dfa-136">Specifies the location for the service.</span></span>
<span data-ttu-id="38dfa-137">Jeśli nie istnieje określona grupa koligacji, wymagana jest lokalizacja.</span><span class="sxs-lookup"><span data-stu-id="38dfa-137">A location is required if there isn't a specified Affinity Group.</span></span>

```yaml
Type: String
Parameter Sets: ParameterSetLocation
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38dfa-138">-Profile</span><span class="sxs-lookup"><span data-stu-id="38dfa-138">-Profile</span></span>
<span data-ttu-id="38dfa-139">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38dfa-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="38dfa-140">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="38dfa-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="38dfa-141">-ReverseDnsFqdn</span><span class="sxs-lookup"><span data-stu-id="38dfa-141">-ReverseDnsFqdn</span></span>
<span data-ttu-id="38dfa-142">Określa w pełni kwalifikowaną nazwę domeny dla zwrotnego DNS.</span><span class="sxs-lookup"><span data-stu-id="38dfa-142">Specifies the fully qualified domain name for reverse DNS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38dfa-143">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="38dfa-143">-ServiceName</span></span>
<span data-ttu-id="38dfa-144">Określa nazwę nowej usługi.</span><span class="sxs-lookup"><span data-stu-id="38dfa-144">Specifies the name of the new service.</span></span>
<span data-ttu-id="38dfa-145">Nazwa musi być unikatowa dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="38dfa-145">The name must be unique to the subscription.</span></span>

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

### <span data-ttu-id="38dfa-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38dfa-146">CommonParameters</span></span>
<span data-ttu-id="38dfa-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38dfa-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38dfa-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38dfa-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38dfa-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="38dfa-149">INPUTS</span></span>

## <span data-ttu-id="38dfa-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="38dfa-150">OUTPUTS</span></span>

## <span data-ttu-id="38dfa-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="38dfa-151">NOTES</span></span>

## <span data-ttu-id="38dfa-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="38dfa-152">RELATED LINKS</span></span>

[<span data-ttu-id="38dfa-153">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="38dfa-153">Get-AzureService</span></span>](./Get-AzureService.md)

[<span data-ttu-id="38dfa-154">Set-AzureService</span><span class="sxs-lookup"><span data-stu-id="38dfa-154">Set-AzureService</span></span>](./Set-AzureService.md)


