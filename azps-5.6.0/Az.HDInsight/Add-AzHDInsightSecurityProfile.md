---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FB37494B-4035-45B7-88AB-DF33CEEF0D0A
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/add-azhdinsightsecurityprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightSecurityProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightSecurityProfile.md
ms.openlocfilehash: 5ecbf4331412bc35245cad37fb6e24b706233fe1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990151"
---
# <span data-ttu-id="2c32a-101">Add-AzHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="2c32a-101">Add-AzHDInsightSecurityProfile</span></span>

## <span data-ttu-id="2c32a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c32a-102">SYNOPSIS</span></span>
<span data-ttu-id="2c32a-103">Dodaje profil zabezpieczeń do obiektu konfiguracji klastrów.</span><span class="sxs-lookup"><span data-stu-id="2c32a-103">Adds a security profile to a cluster configuration object.</span></span>

## <span data-ttu-id="2c32a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2c32a-104">SYNTAX</span></span>

```
Add-AzHDInsightSecurityProfile [-Config] <AzureHDInsightConfig> -DomainResourceId <String>
 -DomainUserCredential <PSCredential> [-OrganizationalUnitDN <String>] -LdapsUrls <String[]>
 [-ClusterUsersGroupDNs <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2c32a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2c32a-105">DESCRIPTION</span></span>
<span data-ttu-id="2c32a-106">Profil zabezpieczeń służy do tworzenia bezpiecznego klastrów przez kerberyzowanie go.</span><span class="sxs-lookup"><span data-stu-id="2c32a-106">Security profile is used to create a secure cluster by kerberizing it.</span></span>
<span data-ttu-id="2c32a-107">Profil zabezpieczeń zawiera konfigurację związaną z dołączanie klastrem do domeny usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2c32a-107">Security profile contains configuration related joining the cluster to Active Directory Domain.</span></span>

## <span data-ttu-id="2c32a-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2c32a-108">EXAMPLES</span></span>

### <span data-ttu-id="2c32a-109">Przykład 1. Dodawanie profilu zabezpieczeń do obiektu konfiguracji klastrów</span><span class="sxs-lookup"><span data-stu-id="2c32a-109">Example 1: Add security profile to the cluster configuration object</span></span>
```
PS C:\> #Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value

PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

#Security profile info
PS C:\> $domain="sampledomain.onmicrosoft.com"
PS C:\> $domainUser="sample.user@sampledomain.onmicrosoft.com"
PS C:\> $domainPassword=ConvertTo-SecureString "domainPassword" -AsPlainText -Force
PS C:\> $domainUserCredential=New-Object System.Management.Automation.PSCredential($domainUser, $domainPassword)
PS C:\> $organizationalUnitDN="ou=testunitdn"
PS C:\> $ldapsUrls=("ldaps://sampledomain.onmicrosoft.com:636","ldaps://sampledomain.onmicrosoft.com:389")
PS C:\> $clusterUsersGroupDNs=("groupdn1","groupdn2")

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightSecurityProfile `
                -Domain $domain `
                -DomainUserCredential $domainUserCredential `
                -OrganizationalUnitDN $organizationalUnitDN `
                -LdapsUrls $ldapsUrls `
                -ClusterUsersGroupDNs $clusterUsersGroupDNs `
            | New-AzHDInsightCluster `
                -ClusterType Spark `
                -OSType Linux `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageContainer
```

<span data-ttu-id="2c32a-110">To polecenie dodaje wartość profilu zabezpieczeń do klastra o nazwie Twoja-hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="2c32a-110">This command adds a security profile value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="2c32a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c32a-111">PARAMETERS</span></span>

### <span data-ttu-id="2c32a-112">-ClusterUsersGroupDNs</span><span class="sxs-lookup"><span data-stu-id="2c32a-112">-ClusterUsersGroupDNs</span></span>
<span data-ttu-id="2c32a-113">Nazwy odróżniane grup usługi Active Directory, które będą dostępne w zakresach Ambari i Ranger</span><span class="sxs-lookup"><span data-stu-id="2c32a-113">Distinguished names of the Active Directory groups that will be available in Ambari and Ranger</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c32a-114">-Config</span><span class="sxs-lookup"><span data-stu-id="2c32a-114">-Config</span></span>
<span data-ttu-id="2c32a-115">Określa obiekt konfiguracji klastrów HDInsight, który modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c32a-115">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="2c32a-116">Ten obiekt jest tworzony przez New-AzHDInsightClusterConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c32a-116">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c32a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c32a-117">-DefaultProfile</span></span>
<span data-ttu-id="2c32a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="2c32a-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c32a-119">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="2c32a-119">-DomainResourceId</span></span>
<span data-ttu-id="2c32a-120">Identyfikator zasobu domeny usługi Active Directory dla klastrów.</span><span class="sxs-lookup"><span data-stu-id="2c32a-120">Active Directory domain resource id for the cluster.</span></span>

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

### <span data-ttu-id="2c32a-121">-DomainUserCredential</span><span class="sxs-lookup"><span data-stu-id="2c32a-121">-DomainUserCredential</span></span>
<span data-ttu-id="2c32a-122">Poświadczenia konta użytkownika domeny z wystarczającymi uprawnieniami do tworzenia klastrów.</span><span class="sxs-lookup"><span data-stu-id="2c32a-122">A domain user account credential with sufficient permissions for creating the cluster.</span></span>
<span data-ttu-id="2c32a-123">Nazwa użytkownika powinna być w user@domain formacie</span><span class="sxs-lookup"><span data-stu-id="2c32a-123">Username should be in user@domain format</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c32a-124">-LdapsUrls</span><span class="sxs-lookup"><span data-stu-id="2c32a-124">-LdapsUrls</span></span>
<span data-ttu-id="2c32a-125">Adresy URL jednego lub wielu serwerów LDAPS dla usługi Active Directory</span><span class="sxs-lookup"><span data-stu-id="2c32a-125">Urls of one or multiple LDAPS servers for the Active Directory</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c32a-126">-OrganizationalUnitDN</span><span class="sxs-lookup"><span data-stu-id="2c32a-126">-OrganizationalUnitDN</span></span>
<span data-ttu-id="2c32a-127">Wyróżniona nazwa jednostki organizacyjnej w usłudze Active Directory, w której będą tworzone konta użytkowników i komputerów</span><span class="sxs-lookup"><span data-stu-id="2c32a-127">Distinguished name of the organizational unit in the Active directory where user and computer accounts will be created</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c32a-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2c32a-128">-Confirm</span></span>
<span data-ttu-id="2c32a-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2c32a-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c32a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c32a-130">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c32a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c32a-131">CommonParameters</span></span>
<span data-ttu-id="2c32a-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c32a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c32a-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2c32a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c32a-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2c32a-134">INPUTS</span></span>

### <span data-ttu-id="2c32a-135">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="2c32a-135">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>
## <span data-ttu-id="2c32a-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2c32a-136">OUTPUTS</span></span>

### <span data-ttu-id="2c32a-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="2c32a-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile</span></span>
## <span data-ttu-id="2c32a-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2c32a-138">NOTES</span></span>

## <span data-ttu-id="2c32a-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2c32a-139">RELATED LINKS</span></span>
