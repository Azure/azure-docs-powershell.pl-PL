---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: b378effc289c1e57505cabfce9dcccffb60f3f52
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708635"
---
# <span data-ttu-id="6b130-101">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="6b130-101">New-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="6b130-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6b130-102">SYNOPSIS</span></span>
<span data-ttu-id="6b130-103">Tworzy mapowanie sieci funkcji ASR między dwiema sieciami.</span><span class="sxs-lookup"><span data-stu-id="6b130-103">Creates an ASR network mapping between two networks.</span></span>

## <span data-ttu-id="6b130-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6b130-104">SYNTAX</span></span>

### <span data-ttu-id="6b130-105">EnterpriseToEnterprise (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6b130-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b130-106">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="6b130-106">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping [-AzureToAzure] -Name <String> -PrimaryFabric <ASRFabric>
 -PrimaryAzureNetworkId <String> -RecoveryFabric <ASRFabric> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b130-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="6b130-107">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryAzureNetworkId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6b130-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6b130-108">DESCRIPTION</span></span>
<span data-ttu-id="6b130-109">Polecenie cmdlet **New-AzRecoveryServicesAsrNetworkMapping** uruchamia operację tworzenia mapowania sieciowego funkcji ASR między dwiema sieciami i zwraca obiekt zadania ASR dla zadania ASR użytego do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="6b130-109">The **New-AzRecoveryServicesAsrNetworkMapping** cmdlet starts the operation of creating an ASR network mapping between two networks and returns the ASR job object for the ASR job used to track the operation.</span></span>

## <span data-ttu-id="6b130-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6b130-110">EXAMPLES</span></span>

### <span data-ttu-id="6b130-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6b130-111">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrNetworkMapping -Name $NetworkMapName -PrimaryNetwork $PrimaryNetwork -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="6b130-112">Rozpoczyna operację tworzenia mapowania sieci przy użyciu określonej nazwy, sieci podstawowej i sieci odzyskiwania, a następnie zwraca zadanie ASR, aby śledzić operację.</span><span class="sxs-lookup"><span data-stu-id="6b130-112">Starts the network mapping creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation.</span></span>

### <span data-ttu-id="6b130-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6b130-113">Example 2</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrNetworkMapping -AzToAzure -Name "mappingName" -PrimaryFabric $AzureFabric `
 -PrimaryAzureNetworkId $AzureNetworkId -RecoveryFabric $RecoveryAzureFabric -RecoveryAzureNetworkId $RecoveryNetworkId
```

<span data-ttu-id="6b130-114">Rozpoczyna operację mapowania sieci na potrzeby tworzenia przy użyciu określonej nazwy, sieci podstawowej i sieci odzyskiwania, a następnie zwraca zadanie ASR, aby śledzić operację (scenariusz Azure to Azure).</span><span class="sxs-lookup"><span data-stu-id="6b130-114">Starts the network mapping for creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation(Azure to Azure scenario).</span></span>

## <span data-ttu-id="6b130-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6b130-115">PARAMETERS</span></span>

### <span data-ttu-id="6b130-116">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="6b130-116">-AzureToAzure</span></span>
<span data-ttu-id="6b130-117">{{Fill AzureToAzure Description}}</span><span class="sxs-lookup"><span data-stu-id="6b130-117">{{Fill AzureToAzure Description}}</span></span>

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

### <span data-ttu-id="6b130-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b130-118">-DefaultProfile</span></span>
<span data-ttu-id="6b130-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6b130-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="6b130-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6b130-120">-Name</span></span>
<span data-ttu-id="6b130-121">Nazwa mapowania sieci funkcji ASR do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="6b130-121">Name of the ASR network mapping to create.</span></span>

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

### <span data-ttu-id="6b130-122">-PrimaryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="6b130-122">-PrimaryAzureNetworkId</span></span>
<span data-ttu-id="6b130-123">Określa identyfikator sieci wirtualnej usługi Azure dla sieci podstawowej dla mapowania.</span><span class="sxs-lookup"><span data-stu-id="6b130-123">Specifies the Azure virtual network ID of the primary network for the mapping.</span></span>

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

### <span data-ttu-id="6b130-124">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="6b130-124">-PrimaryFabric</span></span>
<span data-ttu-id="6b130-125">Specifes sieć szkieletową ASR, w której ma zostać utworzone mapowanie.</span><span class="sxs-lookup"><span data-stu-id="6b130-125">Specifes the ASR fabric where mapping should be created.</span></span>

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

### <span data-ttu-id="6b130-126">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="6b130-126">-PrimaryNetwork</span></span>
<span data-ttu-id="6b130-127">Określa podstawowy obiekt sieciowy dla mapowania sieci funkcji ASR.</span><span class="sxs-lookup"><span data-stu-id="6b130-127">Specifies the primary network object for the ASR network mapping.</span></span>

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

### <span data-ttu-id="6b130-128">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="6b130-128">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="6b130-129">Określa identyfikator sieci Azure służący do odzyskania mapowania sieci.</span><span class="sxs-lookup"><span data-stu-id="6b130-129">Specifies the recovery azure network ID for the network mapping.</span></span>

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

### <span data-ttu-id="6b130-130">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="6b130-130">-RecoveryFabric</span></span>
<span data-ttu-id="6b130-131">Obiekt szkieletu usługi Azure Site Recovery odpowiadający regionowi odzyskiwania platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6b130-131">The Azure Site Recovery fabric object corresponding to the recovery Azure region.</span></span>

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

### <span data-ttu-id="6b130-132">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="6b130-132">-RecoveryNetwork</span></span>
<span data-ttu-id="6b130-133">Określa obiekt sieci odzyskiwania dla mapowania sieci funkcji ASR.</span><span class="sxs-lookup"><span data-stu-id="6b130-133">Specifies the recovery network object for the ASR network mapping.</span></span>

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

### <span data-ttu-id="6b130-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6b130-134">-Confirm</span></span>
<span data-ttu-id="6b130-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b130-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b130-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b130-136">-WhatIf</span></span>
<span data-ttu-id="6b130-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b130-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6b130-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6b130-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b130-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b130-139">CommonParameters</span></span>
<span data-ttu-id="6b130-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b130-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b130-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b130-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b130-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6b130-142">INPUTS</span></span>

### <span data-ttu-id="6b130-143">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="6b130-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="6b130-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6b130-144">OUTPUTS</span></span>

### <span data-ttu-id="6b130-145">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="6b130-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6b130-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6b130-146">NOTES</span></span>

## <span data-ttu-id="6b130-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6b130-147">RELATED LINKS</span></span>

[<span data-ttu-id="6b130-148">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="6b130-148">Get-AzRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="6b130-149">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="6b130-149">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzRecoveryServicesAsrNetworkMapping.md)