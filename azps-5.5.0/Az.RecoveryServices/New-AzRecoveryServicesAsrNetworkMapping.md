---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: dca68a4f6315ee124c927d0efb0ff0eb95bf1663
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191371"
---
# <span data-ttu-id="14e79-101">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="14e79-101">New-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="14e79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14e79-102">SYNOPSIS</span></span>
<span data-ttu-id="14e79-103">Tworzy mapowanie sieci asr między dwiema sieciami.</span><span class="sxs-lookup"><span data-stu-id="14e79-103">Creates an ASR network mapping between two networks.</span></span>

## <span data-ttu-id="14e79-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="14e79-104">SYNTAX</span></span>

### <span data-ttu-id="14e79-105">EnterpriseToEnterprise (domyślne)</span><span class="sxs-lookup"><span data-stu-id="14e79-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14e79-106">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="14e79-106">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping [-AzureToAzure] -Name <String> -PrimaryFabric <ASRFabric>
 -PrimaryAzureNetworkId <String> -RecoveryFabric <ASRFabric> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14e79-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="14e79-107">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryAzureNetworkId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="14e79-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="14e79-108">DESCRIPTION</span></span>
<span data-ttu-id="14e79-109">Polecenie cmdlet **New-AzRecoveryServicesAsrNetworkMapping** rozpoczyna operację tworzenia mapowania sieci asr między dwiema sieciami i zwraca obiekt zadania asr dla zadania asr służącego do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="14e79-109">The **New-AzRecoveryServicesAsrNetworkMapping** cmdlet starts the operation of creating an ASR network mapping between two networks and returns the ASR job object for the ASR job used to track the operation.</span></span>

## <span data-ttu-id="14e79-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="14e79-110">EXAMPLES</span></span>

### <span data-ttu-id="14e79-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="14e79-111">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrNetworkMapping -Name $NetworkMapName -PrimaryNetwork $PrimaryNetwork -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="14e79-112">Rozpoczyna operację tworzenia mapowania sieci przy użyciu określonej nazwy, sieci podstawowych i sieci odzyskiwania, a następnie zwraca zadanie asr do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="14e79-112">Starts the network mapping creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation.</span></span>

### <span data-ttu-id="14e79-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="14e79-113">Example 2</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrNetworkMapping -AzureToAzure -Name "mappingName" -PrimaryFabric $AzureFabric `
 -PrimaryAzureNetworkId $AzureNetworkId -RecoveryFabric $RecoveryAzureFabric -RecoveryAzureNetworkId $RecoveryNetworkId
```

<span data-ttu-id="14e79-114">Uruchamia mapowanie sieci na operację tworzenia przy użyciu określonej nazwy, sieci podstawowych i sieci odzyskiwania, a następnie zwraca zadanie asr do śledzenia operacji (scenariusz z Azure do Azure).</span><span class="sxs-lookup"><span data-stu-id="14e79-114">Starts the network mapping for creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation(Azure to Azure scenario).</span></span>

## <span data-ttu-id="14e79-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14e79-115">PARAMETERS</span></span>

### <span data-ttu-id="14e79-116">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="14e79-116">-AzureToAzure</span></span>
<span data-ttu-id="14e79-117">Oflaguj, aby utworzyć scenariusz platformy AzureToAzure.</span><span class="sxs-lookup"><span data-stu-id="14e79-117">Flag to create AzureToAzure scenario.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14e79-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14e79-118">-DefaultProfile</span></span>
<span data-ttu-id="14e79-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="14e79-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="14e79-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="14e79-120">-Name</span></span>
<span data-ttu-id="14e79-121">Nazwa mapowania sieci asr do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="14e79-121">Name of the ASR network mapping to create.</span></span>

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

### <span data-ttu-id="14e79-122">-PrimaryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="14e79-122">-PrimaryAzureNetworkId</span></span>
<span data-ttu-id="14e79-123">Określa identyfikator sieci wirtualnej platformy Azure sieci podstawowej dla mapowania.</span><span class="sxs-lookup"><span data-stu-id="14e79-123">Specifies the Azure virtual network ID of the primary network for the mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14e79-124">- PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="14e79-124">-PrimaryFabric</span></span>
<span data-ttu-id="14e79-125">Określa szkielet ASR, w którym należy utworzyć mapowanie.</span><span class="sxs-lookup"><span data-stu-id="14e79-125">Specifies the ASR fabric where mapping should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14e79-126">— PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="14e79-126">-PrimaryNetwork</span></span>
<span data-ttu-id="14e79-127">Określa podstawowy obiekt sieciowy dla mapowania sieci ASR.</span><span class="sxs-lookup"><span data-stu-id="14e79-127">Specifies the primary network object for the ASR network mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14e79-128">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="14e79-128">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="14e79-129">Określa identyfikator sieci azure odzyskiwania dla mapowania sieci.</span><span class="sxs-lookup"><span data-stu-id="14e79-129">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14e79-130">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="14e79-130">-RecoveryFabric</span></span>
<span data-ttu-id="14e79-131">Obiekt szkieletowy usługi Azure Site Recovery odpowiadający regionowi odzyskiwania platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="14e79-131">The Azure Site Recovery fabric object corresponding to the recovery Azure region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14e79-132">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="14e79-132">-RecoveryNetwork</span></span>
<span data-ttu-id="14e79-133">Określa obiekt sieci odzyskiwania dla mapowania sieci ASR.</span><span class="sxs-lookup"><span data-stu-id="14e79-133">Specifies the recovery network object for the ASR network mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14e79-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="14e79-134">-Confirm</span></span>
<span data-ttu-id="14e79-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="14e79-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14e79-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14e79-136">-WhatIf</span></span>
<span data-ttu-id="14e79-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14e79-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="14e79-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="14e79-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14e79-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14e79-139">CommonParameters</span></span>
<span data-ttu-id="14e79-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14e79-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14e79-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="14e79-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14e79-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14e79-142">INPUTS</span></span>

### <span data-ttu-id="14e79-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="14e79-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="14e79-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14e79-144">OUTPUTS</span></span>

### <span data-ttu-id="14e79-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="14e79-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="14e79-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="14e79-146">NOTES</span></span>

## <span data-ttu-id="14e79-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="14e79-147">RELATED LINKS</span></span>

[<span data-ttu-id="14e79-148">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="14e79-148">Get-AzRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="14e79-149">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="14e79-149">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzRecoveryServicesAsrNetworkMapping.md)
