---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrEvent.md
ms.openlocfilehash: e32f0b1d12b1cb0399ddef04623ac76557c809b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549607"
---
# <span data-ttu-id="3bdc8-101">Get-AzureRmRecoveryServicesAsrEvent</span><span class="sxs-lookup"><span data-stu-id="3bdc8-101">Get-AzureRmRecoveryServicesAsrEvent</span></span>

## <span data-ttu-id="3bdc8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3bdc8-102">SYNOPSIS</span></span>
<span data-ttu-id="3bdc8-103">Pobiera szczegóły zdarzeń odzyskiwania witryny Azure w magazynie.</span><span class="sxs-lookup"><span data-stu-id="3bdc8-103">Gets details of Azure Site Recovery events in the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3bdc8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3bdc8-104">SYNTAX</span></span>

### <span data-ttu-id="3bdc8-105">ByParam (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3bdc8-105">ByParam (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrEvent [-AffectedObjectFriendlyName <String>] [-Fabric <ASRFabric>]
 [-Severity <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bdc8-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3bdc8-106">ByResourceId</span></span>
```
Get-AzureRmRecoveryServicesAsrEvent -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3bdc8-107">ByFabricId</span><span class="sxs-lookup"><span data-stu-id="3bdc8-107">ByFabricId</span></span>
```
Get-AzureRmRecoveryServicesAsrEvent -FabricId <String> [-AffectedObjectFriendlyName <String>]
 [-Severity <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bdc8-108">ByName</span><span class="sxs-lookup"><span data-stu-id="3bdc8-108">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrEvent -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3bdc8-109">Opis</span><span class="sxs-lookup"><span data-stu-id="3bdc8-109">DESCRIPTION</span></span>
<span data-ttu-id="3bdc8-110">**Element get-AzureRmRecoveryServicesAsrEvent** pobiera listę zdarzeń w magazynie na podstawie określonych filtrów wyboru.</span><span class="sxs-lookup"><span data-stu-id="3bdc8-110">The **Get-AzureRmRecoveryServicesAsrEvent** gets the list of events in the vault based on the specified selection filters.</span></span>

## <span data-ttu-id="3bdc8-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3bdc8-111">EXAMPLES</span></span>

### <span data-ttu-id="3bdc8-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3bdc8-112">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrEvent
```

<span data-ttu-id="3bdc8-113">Lista wszystkich wydarzeń.</span><span class="sxs-lookup"><span data-stu-id="3bdc8-113">List of all events.</span></span>

### <span data-ttu-id="3bdc8-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="3bdc8-114">Example 2</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrEvent -EventName "VmMonitoringEvent;9091897569816476200_84576304-bafc-4714-8ba6-197a5d09d84f"


AffectedObjectFriendlyName   : V2A-W2K12-400
Description                  : Virtual machine health is in Critical state.
EventCode                    : SRSVMHealthChanged
EventSpecificDetails         :
EventType                    : AgentHealth
FabricId                     : /Subscriptions/xxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxxxxxx/replicationFabrics/xxxxxxxxxxxx
HealthErrors                 : {}
Name                         : VmMonitoringEvent;9091897569816476200_84576304-bafc-4714-8ba6-197a5d09d84f
ProviderSpecificEventDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRInMageAzureV2EventDetails
Severity                     : Critical
TimeOfOccurence              : 8/17/2017 12:31:43 PM
```

<span data-ttu-id="3bdc8-115">Pobierz zdarzenie według nazwy.</span><span class="sxs-lookup"><span data-stu-id="3bdc8-115">Get event by name.</span></span>

### <span data-ttu-id="3bdc8-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="3bdc8-116">Example 3</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxxx
```

<span data-ttu-id="3bdc8-117">Lista zdarzeń związanych z danym obiektem.</span><span class="sxs-lookup"><span data-stu-id="3bdc8-117">List of event for affected Object.</span></span>

### <span data-ttu-id="3bdc8-118">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="3bdc8-118">Example 4</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxx -StartTime "8/17/2017 12:31:40 PM" -EndTime "8/17/2017 12:31:44 PM" -Severity Critical -EventType VmHealth
```

<span data-ttu-id="3bdc8-119">Lista zdarzeń między czasem rozpoczęcia a czasem zakończenia, stanem krytycznym ważności i typem kondycji VmHealth.</span><span class="sxs-lookup"><span data-stu-id="3bdc8-119">List of event between time start time and end time , severity critical and health type VmHealth.</span></span>

## <span data-ttu-id="3bdc8-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3bdc8-120">PARAMETERS</span></span>

### <span data-ttu-id="3bdc8-121">-AffectedObjectFriendlyName</span><span class="sxs-lookup"><span data-stu-id="3bdc8-121">-AffectedObjectFriendlyName</span></span>
<span data-ttu-id="3bdc8-122">Określa przyjazne poleobject dla wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="3bdc8-122">Specifies AffectedObject FriendlyName for the search.</span></span>

```yaml
Type: String
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bdc8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bdc8-123">-DefaultProfile</span></span>
<span data-ttu-id="3bdc8-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3bdc8-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bdc8-125">-EndTime</span><span class="sxs-lookup"><span data-stu-id="3bdc8-125">-EndTime</span></span>
<span data-ttu-id="3bdc8-126">Określa godzinę zakończenia okna wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="3bdc8-126">Specifies the end time of the search window.</span></span> <span data-ttu-id="3bdc8-127">Za pomocą tego parametru można uzyskać tylko te zdarzenia, które wystąpiły przed określonym terminem.</span><span class="sxs-lookup"><span data-stu-id="3bdc8-127">Use this parameter to get only those events that have occurred before the specified time.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bdc8-128">-EventType</span><span class="sxs-lookup"><span data-stu-id="3bdc8-128">-EventType</span></span>
<span data-ttu-id="3bdc8-129">Filtrowanie zdarzeń według typu zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="3bdc8-129">Filter events by the event type.</span></span>

```yaml
Type: String
Parameter Sets: ByParam, ByFabricId
Aliases:
Accepted values: VmHealth, ServerHealth, AgentHealth

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bdc8-130">-Fabric</span><span class="sxs-lookup"><span data-stu-id="3bdc8-130">-Fabric</span></span>
<span data-ttu-id="3bdc8-131">Filtrowanie zdarzeń według określonej sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="3bdc8-131">Filter events by the specified fabric.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bdc8-132">-FabricId</span><span class="sxs-lookup"><span data-stu-id="3bdc8-132">-FabricId</span></span>
<span data-ttu-id="3bdc8-133">Określa fabricId do filtrowania.</span><span class="sxs-lookup"><span data-stu-id="3bdc8-133">Specifies the fabricId to filter.</span></span>

```yaml
Type: String
Parameter Sets: ByFabricId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bdc8-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3bdc8-134">-Name</span></span>
<span data-ttu-id="3bdc8-135">Określa nazwę zdarzenia do wyszukania.</span><span class="sxs-lookup"><span data-stu-id="3bdc8-135">Specifies name of the event for search.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bdc8-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3bdc8-136">-ResourceId</span></span>
<span data-ttu-id="3bdc8-137">Specifes zdarzenie ReourceId zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="3bdc8-137">Specifes the event ReourceId of event.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bdc8-138">— Ważność</span><span class="sxs-lookup"><span data-stu-id="3bdc8-138">-Severity</span></span>
<span data-ttu-id="3bdc8-139">Waga zdarzenia, według którego ma zostać wykonane filtrowanie.</span><span class="sxs-lookup"><span data-stu-id="3bdc8-139">Event severity to filter on.</span></span>

```yaml
Type: String
Parameter Sets: ByParam, ByFabricId
Aliases:
Accepted values: Critical, Warning, OK, Unknown

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bdc8-140">-StartTime</span><span class="sxs-lookup"><span data-stu-id="3bdc8-140">-StartTime</span></span>
<span data-ttu-id="3bdc8-141">Określa godzinę rozpoczęcia okna wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="3bdc8-141">Specifies the start time of the search window.</span></span> <span data-ttu-id="3bdc8-142">Za pomocą tego parametru można pobierać tylko te zdarzenia, które wystąpiły po określonym czasie.</span><span class="sxs-lookup"><span data-stu-id="3bdc8-142">Use this parameter to get only those events that have occurred after the specified time.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bdc8-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bdc8-143">CommonParameters</span></span>
<span data-ttu-id="3bdc8-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bdc8-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bdc8-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bdc8-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bdc8-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3bdc8-146">INPUTS</span></span>

### <span data-ttu-id="3bdc8-147">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="3bdc8-147">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="3bdc8-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3bdc8-148">OUTPUTS</span></span>

### <span data-ttu-id="3bdc8-149">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASREvent, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="3bdc8-149">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASREvent, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="3bdc8-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3bdc8-150">NOTES</span></span>

## <span data-ttu-id="3bdc8-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3bdc8-151">RELATED LINKS</span></span>
