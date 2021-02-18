---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrEvent.md
ms.openlocfilehash: 8ed57766ba36607503994d331cec5381d9f43bbf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193050"
---
# <span data-ttu-id="4c2a1-101">Get-AzRecoveryServicesAsrEvent</span><span class="sxs-lookup"><span data-stu-id="4c2a1-101">Get-AzRecoveryServicesAsrEvent</span></span>

## <span data-ttu-id="4c2a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c2a1-102">SYNOPSIS</span></span>
<span data-ttu-id="4c2a1-103">Pobiera szczegółowe informacje o zdarzeniach odzyskiwania witryny platformy Azure w magazynie.</span><span class="sxs-lookup"><span data-stu-id="4c2a1-103">Gets details of Azure Site Recovery events in the vault.</span></span>

## <span data-ttu-id="4c2a1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4c2a1-104">SYNTAX</span></span>

### <span data-ttu-id="4c2a1-105">ByParam (domyślne)</span><span class="sxs-lookup"><span data-stu-id="4c2a1-105">ByParam (Default)</span></span>
```
Get-AzRecoveryServicesAsrEvent [-AffectedObjectFriendlyName <String>] [-Fabric <ASRFabric>]
 [-Severity <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c2a1-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4c2a1-106">ByResourceId</span></span>
```
Get-AzRecoveryServicesAsrEvent -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4c2a1-107">ByFabricId</span><span class="sxs-lookup"><span data-stu-id="4c2a1-107">ByFabricId</span></span>
```
Get-AzRecoveryServicesAsrEvent -FabricId <String> [-AffectedObjectFriendlyName <String>] [-Severity <String>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4c2a1-108">ByName</span><span class="sxs-lookup"><span data-stu-id="4c2a1-108">ByName</span></span>
```
Get-AzRecoveryServicesAsrEvent -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c2a1-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="4c2a1-109">DESCRIPTION</span></span>
<span data-ttu-id="4c2a1-110">Dodatek **Get-AzRecoveryServicesAsrEvent** pobiera listę zdarzeń w magazynie na podstawie określonych filtrów zaznaczenia.</span><span class="sxs-lookup"><span data-stu-id="4c2a1-110">The **Get-AzRecoveryServicesAsrEvent** gets the list of events in the vault based on the specified selection filters.</span></span>

## <span data-ttu-id="4c2a1-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4c2a1-111">EXAMPLES</span></span>

### <span data-ttu-id="4c2a1-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4c2a1-112">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent
```

<span data-ttu-id="4c2a1-113">Lista wszystkich zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="4c2a1-113">List of all events.</span></span>

### <span data-ttu-id="4c2a1-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="4c2a1-114">Example 2</span></span>
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

<span data-ttu-id="4c2a1-115">Uzyskiwanie zdarzenia według nazwy.</span><span class="sxs-lookup"><span data-stu-id="4c2a1-115">Get event by name.</span></span>

### <span data-ttu-id="4c2a1-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="4c2a1-116">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxxx
```

<span data-ttu-id="4c2a1-117">Lista zdarzeń dla obiektu, którego dotyczy problem.</span><span class="sxs-lookup"><span data-stu-id="4c2a1-117">List of event for affected Object.</span></span>

### <span data-ttu-id="4c2a1-118">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="4c2a1-118">Example 4</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxx -StartTime "8/17/2017 12:31:40 PM" -EndTime "8/17/2017 12:31:44 PM" -Severity Critical -EventType VmHealth
```

<span data-ttu-id="4c2a1-119">Lista zdarzeń między godziną rozpoczęcia i godziną zakończenia, istotność o znaczeniu krytycznym i typ kondycji WMK.</span><span class="sxs-lookup"><span data-stu-id="4c2a1-119">List of event between time start time and end time , severity critical and health type VmHealth.</span></span>

## <span data-ttu-id="4c2a1-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c2a1-120">PARAMETERS</span></span>

### <span data-ttu-id="4c2a1-121">-AffectedObjectFriendlyName</span><span class="sxs-lookup"><span data-stu-id="4c2a1-121">-AffectedObjectFriendlyName</span></span>
<span data-ttu-id="4c2a1-122">Określa przyjazną nazwę dla parametru AffectedObject dla wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="4c2a1-122">Specifies AffectedObject FriendlyName for the search.</span></span>

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

### <span data-ttu-id="4c2a1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c2a1-123">-DefaultProfile</span></span>
<span data-ttu-id="4c2a1-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4c2a1-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c2a1-125">- EndTime</span><span class="sxs-lookup"><span data-stu-id="4c2a1-125">-EndTime</span></span>
<span data-ttu-id="4c2a1-126">Określa czas zakończenia okna wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="4c2a1-126">Specifies the end time of the search window.</span></span> <span data-ttu-id="4c2a1-127">Ten parametr umożliwia uzyskiwanie tylko tych zdarzeń, które wystąpiły przed określonym czasem.</span><span class="sxs-lookup"><span data-stu-id="4c2a1-127">Use this parameter to get only those events that have occurred before the specified time.</span></span>

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

### <span data-ttu-id="4c2a1-128">-EventType</span><span class="sxs-lookup"><span data-stu-id="4c2a1-128">-EventType</span></span>
<span data-ttu-id="4c2a1-129">Filtrowanie zdarzeń według typu zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="4c2a1-129">Filter events by the event type.</span></span>

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

### <span data-ttu-id="4c2a1-130">— Materiał</span><span class="sxs-lookup"><span data-stu-id="4c2a1-130">-Fabric</span></span>
<span data-ttu-id="4c2a1-131">Filtrowanie zdarzeń według określonego materiału.</span><span class="sxs-lookup"><span data-stu-id="4c2a1-131">Filter events by the specified fabric.</span></span>

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

### <span data-ttu-id="4c2a1-132">- FabricId</span><span class="sxs-lookup"><span data-stu-id="4c2a1-132">-FabricId</span></span>
<span data-ttu-id="4c2a1-133">Określa wartość określającą wartość fabricId do filtrowania.</span><span class="sxs-lookup"><span data-stu-id="4c2a1-133">Specifies the fabricId to filter.</span></span>

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

### <span data-ttu-id="4c2a1-134">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4c2a1-134">-Name</span></span>
<span data-ttu-id="4c2a1-135">Określa nazwę zdarzenia do wyszukania.</span><span class="sxs-lookup"><span data-stu-id="4c2a1-135">Specifies name of the event for search.</span></span>

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

### <span data-ttu-id="4c2a1-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4c2a1-136">-ResourceId</span></span>
<span data-ttu-id="4c2a1-137">Określa zdarzenie ResourceId zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="4c2a1-137">Specifies the event ResourceId of event.</span></span>

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

### <span data-ttu-id="4c2a1-138">— Ważność</span><span class="sxs-lookup"><span data-stu-id="4c2a1-138">-Severity</span></span>
<span data-ttu-id="4c2a1-139">Ważność zdarzenia, według których należy filtrować.</span><span class="sxs-lookup"><span data-stu-id="4c2a1-139">Event severity to filter on.</span></span>

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

### <span data-ttu-id="4c2a1-140">— StartTime</span><span class="sxs-lookup"><span data-stu-id="4c2a1-140">-StartTime</span></span>
<span data-ttu-id="4c2a1-141">Określa czas rozpoczęcia okna wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="4c2a1-141">Specifies the start time of the search window.</span></span> <span data-ttu-id="4c2a1-142">Ten parametr umożliwia uzyskiwanie tylko tych zdarzeń, które wystąpiły po określonym czasie.</span><span class="sxs-lookup"><span data-stu-id="4c2a1-142">Use this parameter to get only those events that have occurred after the specified time.</span></span>

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

### <span data-ttu-id="4c2a1-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c2a1-143">CommonParameters</span></span>
<span data-ttu-id="4c2a1-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c2a1-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c2a1-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4c2a1-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c2a1-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4c2a1-146">INPUTS</span></span>

### <span data-ttu-id="4c2a1-147">System.String</span><span class="sxs-lookup"><span data-stu-id="4c2a1-147">System.String</span></span>

## <span data-ttu-id="4c2a1-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4c2a1-148">OUTPUTS</span></span>

### <span data-ttu-id="4c2a1-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASREvent</span><span class="sxs-lookup"><span data-stu-id="4c2a1-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASREvent</span></span>

## <span data-ttu-id="4c2a1-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4c2a1-150">NOTES</span></span>

## <span data-ttu-id="4c2a1-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4c2a1-151">RELATED LINKS</span></span>
