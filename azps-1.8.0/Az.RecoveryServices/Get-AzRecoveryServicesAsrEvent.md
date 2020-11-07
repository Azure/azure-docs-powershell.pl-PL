---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrEvent.md
ms.openlocfilehash: 0c7b80c77d91f8b92fc4ab03f715412ac061b9fd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708710"
---
# <span data-ttu-id="23fbe-101">Get-AzRecoveryServicesAsrEvent</span><span class="sxs-lookup"><span data-stu-id="23fbe-101">Get-AzRecoveryServicesAsrEvent</span></span>

## <span data-ttu-id="23fbe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="23fbe-102">SYNOPSIS</span></span>
<span data-ttu-id="23fbe-103">Pobiera szczegóły zdarzeń odzyskiwania witryny Azure w magazynie.</span><span class="sxs-lookup"><span data-stu-id="23fbe-103">Gets details of Azure Site Recovery events in the vault.</span></span>

## <span data-ttu-id="23fbe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="23fbe-104">SYNTAX</span></span>

### <span data-ttu-id="23fbe-105">ByParam (domyślny)</span><span class="sxs-lookup"><span data-stu-id="23fbe-105">ByParam (Default)</span></span>
```
Get-AzRecoveryServicesAsrEvent [-AffectedObjectFriendlyName <String>] [-Fabric <ASRFabric>]
 [-Severity <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23fbe-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="23fbe-106">ByResourceId</span></span>
```
Get-AzRecoveryServicesAsrEvent -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="23fbe-107">ByFabricId</span><span class="sxs-lookup"><span data-stu-id="23fbe-107">ByFabricId</span></span>
```
Get-AzRecoveryServicesAsrEvent -FabricId <String> [-AffectedObjectFriendlyName <String>] [-Severity <String>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="23fbe-108">ByName</span><span class="sxs-lookup"><span data-stu-id="23fbe-108">ByName</span></span>
```
Get-AzRecoveryServicesAsrEvent -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23fbe-109">Opis</span><span class="sxs-lookup"><span data-stu-id="23fbe-109">DESCRIPTION</span></span>
<span data-ttu-id="23fbe-110">**Element get-AzRecoveryServicesAsrEvent** pobiera listę zdarzeń w magazynie na podstawie określonych filtrów wyboru.</span><span class="sxs-lookup"><span data-stu-id="23fbe-110">The **Get-AzRecoveryServicesAsrEvent** gets the list of events in the vault based on the specified selection filters.</span></span>

## <span data-ttu-id="23fbe-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="23fbe-111">EXAMPLES</span></span>

### <span data-ttu-id="23fbe-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="23fbe-112">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent
```

<span data-ttu-id="23fbe-113">Lista wszystkich wydarzeń.</span><span class="sxs-lookup"><span data-stu-id="23fbe-113">List of all events.</span></span>

### <span data-ttu-id="23fbe-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="23fbe-114">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent -EventName "VmMonitoringEvent;9091897569816476200_84576304-bafc-4714-8ba6-197a5d09d84f"


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

<span data-ttu-id="23fbe-115">Pobierz zdarzenie według nazwy.</span><span class="sxs-lookup"><span data-stu-id="23fbe-115">Get event by name.</span></span>

### <span data-ttu-id="23fbe-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="23fbe-116">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxxx
```

<span data-ttu-id="23fbe-117">Lista zdarzeń związanych z danym obiektem.</span><span class="sxs-lookup"><span data-stu-id="23fbe-117">List of event for affected Object.</span></span>

### <span data-ttu-id="23fbe-118">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="23fbe-118">Example 4</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxx -StartTime "8/17/2017 12:31:40 PM" -EndTime "8/17/2017 12:31:44 PM" -Severity Critical -EventType VmHealth
```

<span data-ttu-id="23fbe-119">Lista zdarzeń między czasem rozpoczęcia a czasem zakończenia, stanem krytycznym ważności i typem kondycji VmHealth.</span><span class="sxs-lookup"><span data-stu-id="23fbe-119">List of event between time start time and end time , severity critical and health type VmHealth.</span></span>

## <span data-ttu-id="23fbe-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="23fbe-120">PARAMETERS</span></span>

### <span data-ttu-id="23fbe-121">-AffectedObjectFriendlyName</span><span class="sxs-lookup"><span data-stu-id="23fbe-121">-AffectedObjectFriendlyName</span></span>
<span data-ttu-id="23fbe-122">Określa przyjazne poleobject dla wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="23fbe-122">Specifies AffectedObject FriendlyName for the search.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23fbe-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23fbe-123">-DefaultProfile</span></span>
<span data-ttu-id="23fbe-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="23fbe-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23fbe-125">-EndTime</span><span class="sxs-lookup"><span data-stu-id="23fbe-125">-EndTime</span></span>
<span data-ttu-id="23fbe-126">Określa godzinę zakończenia okna wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="23fbe-126">Specifies the end time of the search window.</span></span> <span data-ttu-id="23fbe-127">Za pomocą tego parametru można uzyskać tylko te zdarzenia, które wystąpiły przed określonym terminem.</span><span class="sxs-lookup"><span data-stu-id="23fbe-127">Use this parameter to get only those events that have occurred before the specified time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23fbe-128">-EventType</span><span class="sxs-lookup"><span data-stu-id="23fbe-128">-EventType</span></span>
<span data-ttu-id="23fbe-129">Filtrowanie zdarzeń według typu zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="23fbe-129">Filter events by the event type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam, ByFabricId
Aliases:
Accepted values: VmHealth, ServerHealth, AgentHealth

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23fbe-130">-Fabric</span><span class="sxs-lookup"><span data-stu-id="23fbe-130">-Fabric</span></span>
<span data-ttu-id="23fbe-131">Filtrowanie zdarzeń według określonej sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="23fbe-131">Filter events by the specified fabric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23fbe-132">-FabricId</span><span class="sxs-lookup"><span data-stu-id="23fbe-132">-FabricId</span></span>
<span data-ttu-id="23fbe-133">Określa fabricId do filtrowania.</span><span class="sxs-lookup"><span data-stu-id="23fbe-133">Specifies the fabricId to filter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFabricId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23fbe-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="23fbe-134">-Name</span></span>
<span data-ttu-id="23fbe-135">Określa nazwę zdarzenia do wyszukania.</span><span class="sxs-lookup"><span data-stu-id="23fbe-135">Specifies name of the event for search.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23fbe-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23fbe-136">-ResourceId</span></span>
<span data-ttu-id="23fbe-137">Specifes zdarzenie ReourceId zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="23fbe-137">Specifes the event ReourceId of event.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23fbe-138">— Ważność</span><span class="sxs-lookup"><span data-stu-id="23fbe-138">-Severity</span></span>
<span data-ttu-id="23fbe-139">Waga zdarzenia, według którego ma zostać wykonane filtrowanie.</span><span class="sxs-lookup"><span data-stu-id="23fbe-139">Event severity to filter on.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam, ByFabricId
Aliases:
Accepted values: Critical, Warning, OK, Unknown

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23fbe-140">-StartTime</span><span class="sxs-lookup"><span data-stu-id="23fbe-140">-StartTime</span></span>
<span data-ttu-id="23fbe-141">Określa godzinę rozpoczęcia okna wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="23fbe-141">Specifies the start time of the search window.</span></span> <span data-ttu-id="23fbe-142">Za pomocą tego parametru można pobierać tylko te zdarzenia, które wystąpiły po określonym czasie.</span><span class="sxs-lookup"><span data-stu-id="23fbe-142">Use this parameter to get only those events that have occurred after the specified time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23fbe-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23fbe-143">CommonParameters</span></span>
<span data-ttu-id="23fbe-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23fbe-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23fbe-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23fbe-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23fbe-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23fbe-146">INPUTS</span></span>

### <span data-ttu-id="23fbe-147">System. String</span><span class="sxs-lookup"><span data-stu-id="23fbe-147">System.String</span></span>

## <span data-ttu-id="23fbe-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="23fbe-148">OUTPUTS</span></span>

### <span data-ttu-id="23fbe-149">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASREvent</span><span class="sxs-lookup"><span data-stu-id="23fbe-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASREvent</span></span>

## <span data-ttu-id="23fbe-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="23fbe-150">NOTES</span></span>

## <span data-ttu-id="23fbe-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="23fbe-151">RELATED LINKS</span></span>