---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 01AE09A8-B779-475A-9E86-776E0774E89E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetworkMapping.md
ms.openlocfilehash: d9a1e26691ab0ea1be04365747f97d8fc6111672
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545995"
---
# <span data-ttu-id="be92d-101">Get-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="be92d-101">Get-AzureRmSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="be92d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="be92d-102">SYNOPSIS</span></span>
<span data-ttu-id="be92d-103">Pobiera informacje o mapowaniach sieciowych odzyskiwania witryny dla bieżącego magazynu.</span><span class="sxs-lookup"><span data-stu-id="be92d-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be92d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="be92d-104">SYNTAX</span></span>

### <span data-ttu-id="be92d-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="be92d-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be92d-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="be92d-106">EnterpriseToEnterprise</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be92d-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="be92d-107">EnterpriseToAzure</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping -PrimaryFabric <ASRFabric> [-Azure]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be92d-108">EnterpriseToAzureLegacy</span><span class="sxs-lookup"><span data-stu-id="be92d-108">EnterpriseToAzureLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping [-Azure] -PrimaryServer <ASRServer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be92d-109">EnterpriseToEnterpriseLegacy</span><span class="sxs-lookup"><span data-stu-id="be92d-109">EnterpriseToEnterpriseLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be92d-110">Opis</span><span class="sxs-lookup"><span data-stu-id="be92d-110">DESCRIPTION</span></span>
<span data-ttu-id="be92d-111">Polecenie cmdlet **Get-AzureRmSiteRecoveryNetworkMapping** pobiera informacje o mapowaniach sieciowych usługi Azure Site Recovery dla bieżącego magazynu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="be92d-111">The **Get-AzureRmSiteRecoveryNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the current Site Recovery vault.</span></span>

## <span data-ttu-id="be92d-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="be92d-112">EXAMPLES</span></span>

## <span data-ttu-id="be92d-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="be92d-113">PARAMETERS</span></span>

### <span data-ttu-id="be92d-114">-Azure</span><span class="sxs-lookup"><span data-stu-id="be92d-114">-Azure</span></span>
<span data-ttu-id="be92d-115">Wskazuje, że polecenie pobiera listę mapowań sieciowych dla sieci na serwerze podstawowym zamapowanym na wirtualne sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="be92d-115">Indicates that the command gets a list of network mappings for networks on the primary server mapped to Azure virtual networks.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToAzure, EnterpriseToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be92d-116">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="be92d-116">-PrimaryFabric</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be92d-117">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="be92d-117">-PrimaryServer</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: EnterpriseToAzureLegacy, EnterpriseToEnterpriseLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be92d-118">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="be92d-118">-RecoveryFabric</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be92d-119">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="be92d-119">-RecoveryServer</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: EnterpriseToEnterpriseLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be92d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be92d-120">-DefaultProfile</span></span>
<span data-ttu-id="be92d-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="be92d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be92d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be92d-122">CommonParameters</span></span>
<span data-ttu-id="be92d-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be92d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be92d-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be92d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be92d-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be92d-125">INPUTS</span></span>

### <span data-ttu-id="be92d-126">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="be92d-126">ASRFabric</span></span>
<span data-ttu-id="be92d-127">Parametr "PrimaryFabric" akceptuje wartość typu "ASRFabric" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="be92d-127">Parameter 'PrimaryFabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

### <span data-ttu-id="be92d-128">ASRServer</span><span class="sxs-lookup"><span data-stu-id="be92d-128">ASRServer</span></span>
<span data-ttu-id="be92d-129">Parametr "PrimaryServer" akceptuje wartość typu "ASRServer" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="be92d-129">Parameter 'PrimaryServer' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="be92d-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="be92d-130">OUTPUTS</span></span>

### <span data-ttu-id="be92d-131">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRNetworkMapping]</span><span class="sxs-lookup"><span data-stu-id="be92d-131">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRNetworkMapping]</span></span>

## <span data-ttu-id="be92d-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="be92d-132">NOTES</span></span>

## <span data-ttu-id="be92d-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="be92d-133">RELATED LINKS</span></span>

[<span data-ttu-id="be92d-134">Nowe — AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="be92d-134">New-AzureRmSiteRecoveryNetworkMapping</span></span>](./New-AzureRmSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="be92d-135">Remove-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="be92d-135">Remove-AzureRmSiteRecoveryNetworkMapping</span></span>](./Remove-AzureRmSiteRecoveryNetworkMapping.md)
