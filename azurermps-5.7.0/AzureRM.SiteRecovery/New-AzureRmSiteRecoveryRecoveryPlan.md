---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 1166EC21-5626-41F6-9CCE-2169CF202575
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoveryrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: 8aba5d85e11a6494c4362de4d729c5e7b64106fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551527"
---
# <span data-ttu-id="0545e-101">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0545e-101">New-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="0545e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0545e-102">SYNOPSIS</span></span>
<span data-ttu-id="0545e-103">Tworzy plan odzyskiwania witryny w ramach odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="0545e-103">Creates a site recovery plan in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0545e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0545e-104">SYNTAX</span></span>

### <span data-ttu-id="0545e-105">EnterpriseToEnterprise (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0545e-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0545e-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="0545e-106">EnterpriseToAzure</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0545e-107">EnterpriseToEnterpriseLegacy</span><span class="sxs-lookup"><span data-stu-id="0545e-107">EnterpriseToEnterpriseLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 -ProtectionEntityList <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0545e-108">EnterpriseToAzureLegacy</span><span class="sxs-lookup"><span data-stu-id="0545e-108">EnterpriseToAzureLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> [-Azure] -FailoverDeploymentModel <String>
 -PrimaryServer <ASRServer> -ProtectionEntityList <ASRProtectionEntity[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0545e-109">HyperVSiteToAzureLegacy</span><span class="sxs-lookup"><span data-stu-id="0545e-109">HyperVSiteToAzureLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -FailoverDeploymentModel <String> -PrimarySite <ASRSite>
 -ProtectionEntityList <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0545e-110">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="0545e-110">ByRPFile</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0545e-111">Opis</span><span class="sxs-lookup"><span data-stu-id="0545e-111">DESCRIPTION</span></span>
<span data-ttu-id="0545e-112">Polecenie cmdlet **New-AzureRmSiteRecoveryRecoveryPlan** tworzy plan odzyskiwania w usłudze Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="0545e-112">The **New-AzureRmSiteRecoveryRecoveryPlan** cmdlet creates a recovery plan in Azure Site Recovery.</span></span>

<span data-ttu-id="0545e-113">Plan odzyskiwania umożliwia zbieranie maszyn wirtualnych w grupie w celu przejęcia awaryjnego i odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="0545e-113">A recovery plan gathers virtual machines in a group for the purposes of failover and recovery.</span></span>

## <span data-ttu-id="0545e-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0545e-114">EXAMPLES</span></span>

### <span data-ttu-id="0545e-115">Przykład 1: Dodawanie planu odzyskiwania do magazynu odzyskiwania witryny</span><span class="sxs-lookup"><span data-stu-id="0545e-115">Example 1: Add a recovery plan to a Site Recovery vault</span></span>
```
PS C:\>New-AzureRmSiteRecoveryRecoveryPlan -Path "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="0545e-116">To polecenie dodaje plan odzyskiwania o nazwie RecoveryPlan.xml do magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="0545e-116">This command adds the recovery plan named RecoveryPlan.xml to the Azure Site Recovery vault.</span></span>

## <span data-ttu-id="0545e-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0545e-117">PARAMETERS</span></span>

### <span data-ttu-id="0545e-118">-Azure</span><span class="sxs-lookup"><span data-stu-id="0545e-118">-Azure</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToAzure, EnterpriseToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0545e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0545e-119">-DefaultProfile</span></span>
<span data-ttu-id="0545e-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0545e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0545e-121">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="0545e-121">-FailoverDeploymentModel</span></span>
```yaml
Type: String
Parameter Sets: EnterpriseToAzure, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 
Accepted values: Classic, ResourceManager

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0545e-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0545e-122">-Name</span></span>
```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0545e-123">-Path</span><span class="sxs-lookup"><span data-stu-id="0545e-123">-Path</span></span>
<span data-ttu-id="0545e-124">Określa ścieżkę pliku planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="0545e-124">Specifies the path of the recovery plan file.</span></span>

```yaml
Type: String
Parameter Sets: ByRPFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0545e-125">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="0545e-125">-PrimaryFabric</span></span>
```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0545e-126">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="0545e-126">-PrimaryServer</span></span>
```yaml
Type: ASRServer
Parameter Sets: EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0545e-127">-PrimarySite</span><span class="sxs-lookup"><span data-stu-id="0545e-127">-PrimarySite</span></span>
```yaml
Type: ASRSite
Parameter Sets: HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0545e-128">-ProtectionEntityList</span><span class="sxs-lookup"><span data-stu-id="0545e-128">-ProtectionEntityList</span></span>
```yaml
Type: ASRProtectionEntity[]
Parameter Sets: EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0545e-129">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="0545e-129">-RecoveryFabric</span></span>
```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0545e-130">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="0545e-130">-RecoveryServer</span></span>
```yaml
Type: ASRServer
Parameter Sets: EnterpriseToEnterpriseLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0545e-131">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="0545e-131">-ReplicationProtectedItem</span></span>
```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0545e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0545e-132">CommonParameters</span></span>
<span data-ttu-id="0545e-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0545e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0545e-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0545e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0545e-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0545e-135">INPUTS</span></span>

### <span data-ttu-id="0545e-136">ASRProtectionEntity[]</span><span class="sxs-lookup"><span data-stu-id="0545e-136">ASRProtectionEntity[]</span></span>
<span data-ttu-id="0545e-137">Parametr "ProtectionEntityList" akceptuje wartość typu "ASRProtectionEntity []" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="0545e-137">Parameter 'ProtectionEntityList' accepts value of type 'ASRProtectionEntity[]' from the pipeline</span></span>

### <span data-ttu-id="0545e-138">ASRReplicationProtectedItem[]</span><span class="sxs-lookup"><span data-stu-id="0545e-138">ASRReplicationProtectedItem[]</span></span>
<span data-ttu-id="0545e-139">Parametr "ReplicationProtectedItem" akceptuje wartość typu "ASRReplicationProtectedItem []" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="0545e-139">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem[]' from the pipeline</span></span>

## <span data-ttu-id="0545e-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0545e-140">OUTPUTS</span></span>

## <span data-ttu-id="0545e-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0545e-141">NOTES</span></span>

## <span data-ttu-id="0545e-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0545e-142">RELATED LINKS</span></span>

[<span data-ttu-id="0545e-143">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0545e-143">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="0545e-144">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0545e-144">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="0545e-145">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0545e-145">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)


