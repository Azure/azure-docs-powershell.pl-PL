---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: BABBA19E-5833-452C-9E36-811EAE7C20F9
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb326281058f0ff9280c4b87c0530241ece801e0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054527"
---
# <span data-ttu-id="3dc62-101">Get-AzureStorSimpleFailoverVolumeContainers</span><span class="sxs-lookup"><span data-stu-id="3dc62-101">Get-AzureStorSimpleFailoverVolumeContainers</span></span>

## <span data-ttu-id="3dc62-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3dc62-102">SYNOPSIS</span></span>
<span data-ttu-id="3dc62-103">Pobiera grupy kontenerów woluminów dla trybu failover urządzenia.</span><span class="sxs-lookup"><span data-stu-id="3dc62-103">Gets the volume container groups for device failover.</span></span>

## <span data-ttu-id="3dc62-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3dc62-104">SYNTAX</span></span>

### <span data-ttu-id="3dc62-105">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="3dc62-105">IdentifyById</span></span>
```
Get-AzureStorSimpleFailoverVolumeContainers -DeviceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3dc62-106">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="3dc62-106">IdentifyByName</span></span>
```
Get-AzureStorSimpleFailoverVolumeContainers -DeviceName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="3dc62-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3dc62-107">DESCRIPTION</span></span>
<span data-ttu-id="3dc62-108">Polecenie cmdlet **Get-AzureStorSimpleFailoverVolumeContainers** umożliwia pobieranie grup kontenerów woluminów dla trybu failover urządzenia.</span><span class="sxs-lookup"><span data-stu-id="3dc62-108">The **Get-AzureStorSimpleFailoverVolumeContainers** cmdlet gets the volume container groups for device failover.</span></span>
<span data-ttu-id="3dc62-109">Przekazanie pojedynczej grupy **VolumeContainer** lub tablicy grup **VolumeContainer** do polecenia cmdlet **Start-AzureStorSimpleDeviceFailover** .</span><span class="sxs-lookup"><span data-stu-id="3dc62-109">Pass a single **VolumeContainer** group or an array of **VolumeContainer** groups to the **Start-AzureStorSimpleDeviceFailover** cmdlet.</span></span>
<span data-ttu-id="3dc62-110">Tylko grupy, które mają wartość $True dla właściwości **IsDCGroupEligibleForDR** , kwalifikują się do przejęcia awaryjnego.</span><span class="sxs-lookup"><span data-stu-id="3dc62-110">Only groups that have a value of $True for the **IsDCGroupEligibleForDR** property are eligible for failover.</span></span>

## <span data-ttu-id="3dc62-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3dc62-111">EXAMPLES</span></span>

### <span data-ttu-id="3dc62-112">Przykład 1: pobieranie kontenerów woluminów w trybie failover</span><span class="sxs-lookup"><span data-stu-id="3dc62-112">Example 1: Get failover volume containers</span></span>
```
PS C:\>Get-AzureStorSimpleFailoverVolumeContainers -DeviceName "ChewD_App7"

DCGroup                    IneligibilityMessage          IsDCGroupEligibleForDR
-------                    --------------------          ----------------------
{VolumeContainer1889078...                                                 True
{VC_01}                    No cloud snapshot found                        False
{VolumeContainer7306959}   No cloud snapshot found                        False
{VolumeContainer407850151} No cloud snapshot found                        False
```

<span data-ttu-id="3dc62-113">To polecenie umożliwia przejęcie pracy awaryjnej kontenery woluminów.</span><span class="sxs-lookup"><span data-stu-id="3dc62-113">This command gets failover volume containers.</span></span>
<span data-ttu-id="3dc62-114">W przypadku pracy awaryjnej urządzenia można użyć tylko DCGroups z wartością $True dla właściwości **IsDCGroupEligibleForDR** .</span><span class="sxs-lookup"><span data-stu-id="3dc62-114">Only the DCGroups that have a value of $True for the **IsDCGroupEligibleForDR** property can be used for device failover.</span></span>

## <span data-ttu-id="3dc62-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3dc62-115">PARAMETERS</span></span>

### <span data-ttu-id="3dc62-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="3dc62-116">-DeviceId</span></span>
<span data-ttu-id="3dc62-117">Określa identyfikator wystąpienia urządzenia StorSimple, na którym ma być uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3dc62-117">Specifies the instance ID of the StorSimple device on which to run the cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dc62-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="3dc62-118">-DeviceName</span></span>
<span data-ttu-id="3dc62-119">Określa nazwę urządzenia StorSimple, na którym ma być uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3dc62-119">Specifies the name of the StorSimple device on which to run the cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dc62-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="3dc62-120">-Profile</span></span>
<span data-ttu-id="3dc62-121">Określa Profil platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3dc62-121">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="3dc62-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dc62-122">CommonParameters</span></span>
<span data-ttu-id="3dc62-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dc62-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dc62-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dc62-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dc62-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3dc62-125">INPUTS</span></span>

## <span data-ttu-id="3dc62-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3dc62-126">OUTPUTS</span></span>

### <span data-ttu-id="3dc62-127">IList\<DataContainerGroup\></span><span class="sxs-lookup"><span data-stu-id="3dc62-127">IList\<DataContainerGroup\></span></span>
<span data-ttu-id="3dc62-128">To polecenie cmdlet zwraca listę grup **VolumeContainer** .</span><span class="sxs-lookup"><span data-stu-id="3dc62-128">This cmdlet returns a list of **VolumeContainer** groups.</span></span>

## <span data-ttu-id="3dc62-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3dc62-129">NOTES</span></span>

## <span data-ttu-id="3dc62-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3dc62-130">RELATED LINKS</span></span>

[<span data-ttu-id="3dc62-131">Start — AzureStorSimpleDeviceFailoverJob</span><span class="sxs-lookup"><span data-stu-id="3dc62-131">Start-AzureStorSimpleDeviceFailoverJob</span></span>](./Start-AzureStorSimpleDeviceFailoverJob.md)

[<span data-ttu-id="3dc62-132">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="3dc62-132">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)


