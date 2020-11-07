---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: e9aadbc8eae9703340043dc640f4cb9759b919d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93710924"
---
# <span data-ttu-id="3edc1-101">New-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="3edc1-101">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="3edc1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3edc1-102">SYNOPSIS</span></span>
<span data-ttu-id="3edc1-103">Tworzy mapowanie sieci funkcji ASR między dwiema sieciami.</span><span class="sxs-lookup"><span data-stu-id="3edc1-103">Creates an ASR network mapping between two networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3edc1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3edc1-104">SYNTAX</span></span>

### <span data-ttu-id="3edc1-105">EnterpriseToEnterprise (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3edc1-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3edc1-106">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="3edc1-106">AzureToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping [-AzureToAzure] -Name <String> -PrimaryFabric <ASRFabric>
 -PrimaryAzureNetworkId <String> -RecoveryFabric <ASRFabric> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3edc1-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="3edc1-107">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryAzureNetworkId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3edc1-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3edc1-108">DESCRIPTION</span></span>
<span data-ttu-id="3edc1-109">Polecenie cmdlet **New-AzureRmRecoveryServicesAsrNetworkMapping** uruchamia operację tworzenia mapowania sieciowego funkcji ASR między dwiema sieciami i zwraca obiekt zadania ASR dla zadania ASR użytego do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="3edc1-109">The **New-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet starts the operation of creating an ASR network mapping between two networks and returns the ASR job object for the ASR job used to track the operation.</span></span>

## <span data-ttu-id="3edc1-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3edc1-110">EXAMPLES</span></span>

### <span data-ttu-id="3edc1-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3edc1-111">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrNetworkMapping -Name $NetworkMapName -PrimaryNetwork $PrimaryNetwork -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="3edc1-112">Rozpoczyna operację tworzenia mapowania sieci przy użyciu określonej nazwy, sieci podstawowej i sieci odzyskiwania, a następnie zwraca zadanie ASR, aby śledzić operację.</span><span class="sxs-lookup"><span data-stu-id="3edc1-112">Starts the network mapping creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation.</span></span>

### <span data-ttu-id="3edc1-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="3edc1-113">Example 2</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrNetworkMapping -AzureToAzure -Name "mappingName" -PrimaryFabric $AzureFabric `
 -PrimaryAzureNetworkId $AzureNetworkId -RecoveryFabric $RecoveryAzureFabric -RecoveryAzureNetworkId $RecoveryNetworkId
```

<span data-ttu-id="3edc1-114">Rozpoczyna operację mapowania sieci na potrzeby tworzenia przy użyciu określonej nazwy, sieci podstawowej i sieci odzyskiwania, a następnie zwraca zadanie ASR, aby śledzić operację (scenariusz Azure to Azure).</span><span class="sxs-lookup"><span data-stu-id="3edc1-114">Starts the network mapping for creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation(Azure to Azure scenario).</span></span>

## <span data-ttu-id="3edc1-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3edc1-115">PARAMETERS</span></span>

### <span data-ttu-id="3edc1-116">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="3edc1-116">-AzureToAzure</span></span>
<span data-ttu-id="3edc1-117">Parametr Switch określający, że tworzone mapowanie sieci będzie używane do replikowania maszyn wirtualnych platformy Azure między dwoma regionami platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3edc1-117">Switch parameter specifying that the network mapping being created will be used to replicated Azure virtual machines between two Azure regions.</span></span>

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

### <span data-ttu-id="3edc1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3edc1-118">-DefaultProfile</span></span>
<span data-ttu-id="3edc1-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3edc1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3edc1-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3edc1-120">-Name</span></span>
<span data-ttu-id="3edc1-121">Nazwa mapowania sieci funkcji ASR do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="3edc1-121">Name of the ASR network mapping to create.</span></span>

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

### <span data-ttu-id="3edc1-122">-PrimaryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="3edc1-122">-PrimaryAzureNetworkId</span></span>
<span data-ttu-id="3edc1-123">Określa identyfikator sieci wirtualnej usługi Azure dla sieci podstawowej dla mapowania.</span><span class="sxs-lookup"><span data-stu-id="3edc1-123">Specifies the Azure virtual network ID of the primary network for the mapping.</span></span>

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

### <span data-ttu-id="3edc1-124">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="3edc1-124">-PrimaryFabric</span></span>
<span data-ttu-id="3edc1-125">Specifes sieć szkieletową ASR, w której ma zostać utworzone mapowanie.</span><span class="sxs-lookup"><span data-stu-id="3edc1-125">Specifes the ASR fabric where mapping should be created.</span></span>

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

### <span data-ttu-id="3edc1-126">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="3edc1-126">-PrimaryNetwork</span></span>
<span data-ttu-id="3edc1-127">Określa podstawowy obiekt sieciowy dla mapowania sieci funkcji ASR.</span><span class="sxs-lookup"><span data-stu-id="3edc1-127">Specifies the primary network object for the ASR network mapping.</span></span>

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

### <span data-ttu-id="3edc1-128">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="3edc1-128">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="3edc1-129">Określa identyfikator sieci Azure służący do odzyskania mapowania sieci.</span><span class="sxs-lookup"><span data-stu-id="3edc1-129">Specifies the recovery azure network ID for the network mapping.</span></span>

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

### <span data-ttu-id="3edc1-130">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="3edc1-130">-RecoveryFabric</span></span>
<span data-ttu-id="3edc1-131">Obiekt szkieletu usługi Azure Site Recovery odpowiadający regionowi odzyskiwania platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3edc1-131">The Azure Site Recovery fabric object corresponding to the recovery Azure region.</span></span>

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

### <span data-ttu-id="3edc1-132">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="3edc1-132">-RecoveryNetwork</span></span>
<span data-ttu-id="3edc1-133">Określa obiekt sieci odzyskiwania dla mapowania sieci funkcji ASR.</span><span class="sxs-lookup"><span data-stu-id="3edc1-133">Specifies the recovery network object for the ASR network mapping.</span></span>

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

### <span data-ttu-id="3edc1-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3edc1-134">-Confirm</span></span>
<span data-ttu-id="3edc1-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3edc1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3edc1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3edc1-136">-WhatIf</span></span>
<span data-ttu-id="3edc1-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3edc1-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3edc1-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3edc1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3edc1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3edc1-139">CommonParameters</span></span>
<span data-ttu-id="3edc1-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3edc1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3edc1-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3edc1-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3edc1-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3edc1-142">INPUTS</span></span>

### <span data-ttu-id="3edc1-143">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="3edc1-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="3edc1-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3edc1-144">OUTPUTS</span></span>

### <span data-ttu-id="3edc1-145">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="3edc1-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3edc1-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3edc1-146">NOTES</span></span>

## <span data-ttu-id="3edc1-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3edc1-147">RELATED LINKS</span></span>

[<span data-ttu-id="3edc1-148">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="3edc1-148">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="3edc1-149">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="3edc1-149">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrNetworkMapping.md)