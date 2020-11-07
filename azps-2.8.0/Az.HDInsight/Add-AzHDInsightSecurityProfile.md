---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FB37494B-4035-45B7-88AB-DF33CEEF0D0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightsecurityprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightSecurityProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightSecurityProfile.md
ms.openlocfilehash: c0e54e92336b7b084448a980f632c886c24dc07c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705349"
---
# <span data-ttu-id="fee89-101">Add-AzHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="fee89-101">Add-AzHDInsightSecurityProfile</span></span>

## <span data-ttu-id="fee89-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fee89-102">SYNOPSIS</span></span>
<span data-ttu-id="fee89-103">Dodaje profil zabezpieczeń do obiektu konfiguracji klastra.</span><span class="sxs-lookup"><span data-stu-id="fee89-103">Adds a security profile to a cluster configuration object.</span></span>

## <span data-ttu-id="fee89-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fee89-104">SYNTAX</span></span>

```
Add-AzHDInsightSecurityProfile [-Config] <AzureHDInsightConfig> -Domain <String>
 -DomainUserCredential <PSCredential> -OrganizationalUnitDN <String> -LdapsUrls <String[]>
 [-ClusterUsersGroupDNs <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fee89-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fee89-105">DESCRIPTION</span></span>
<span data-ttu-id="fee89-106">Profil zabezpieczeń służy do tworzenia bezpiecznego klastra przez kerberizing go.</span><span class="sxs-lookup"><span data-stu-id="fee89-106">Security profile is used to create a secure cluster by kerberizing it.</span></span>
<span data-ttu-id="fee89-107">Profil zabezpieczeń zawiera konfigurację powiązana z dołączeniem klastra do domeny usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="fee89-107">Security profile contains configuration related joining the cluster to Active Directory Domain.</span></span>

## <span data-ttu-id="fee89-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fee89-108">EXAMPLES</span></span>

### <span data-ttu-id="fee89-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fee89-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="fee89-110">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="fee89-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="fee89-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fee89-111">PARAMETERS</span></span>

### <span data-ttu-id="fee89-112">-ClusterUsersGroupDNs</span><span class="sxs-lookup"><span data-stu-id="fee89-112">-ClusterUsersGroupDNs</span></span>
<span data-ttu-id="fee89-113">Nazwy wyróżniające grup usługi Active Directory, które będą dostępne w Ambari i Ranger</span><span class="sxs-lookup"><span data-stu-id="fee89-113">Distinguished names of the Active Directory groups that will be available in Ambari and Ranger</span></span>

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

### <span data-ttu-id="fee89-114">-Config</span><span class="sxs-lookup"><span data-stu-id="fee89-114">-Config</span></span>
<span data-ttu-id="fee89-115">Określa obiekt konfiguracji klastra usługi HDInsight, który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fee89-115">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="fee89-116">Ten obiekt jest tworzony za pomocą polecenia cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="fee89-116">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="fee89-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fee89-117">-DefaultProfile</span></span>
<span data-ttu-id="fee89-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="fee89-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fee89-119">-Domain</span><span class="sxs-lookup"><span data-stu-id="fee89-119">-Domain</span></span>
<span data-ttu-id="fee89-120">Domena usługi Active Directory dla klastra</span><span class="sxs-lookup"><span data-stu-id="fee89-120">Active Directory domain for the cluster</span></span>

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

### <span data-ttu-id="fee89-121">-DomainUserCredential</span><span class="sxs-lookup"><span data-stu-id="fee89-121">-DomainUserCredential</span></span>
<span data-ttu-id="fee89-122">Poświadczenia konta użytkownika domeny z odpowiednimi uprawnieniami do tworzenia klastra.</span><span class="sxs-lookup"><span data-stu-id="fee89-122">A domain user account credential with sufficient permissions for creating the cluster.</span></span>
<span data-ttu-id="fee89-123">Nazwa użytkownika powinna być w user@domain formacie</span><span class="sxs-lookup"><span data-stu-id="fee89-123">Username should be in user@domain format</span></span>

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

### <span data-ttu-id="fee89-124">-LdapsUrls</span><span class="sxs-lookup"><span data-stu-id="fee89-124">-LdapsUrls</span></span>
<span data-ttu-id="fee89-125">Adresy URL jednego lub wielu serwerów LDAP dla usługi Active Directory</span><span class="sxs-lookup"><span data-stu-id="fee89-125">Urls of one or multiple LDAPS servers for the Active Directory</span></span>

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

### <span data-ttu-id="fee89-126">-OrganizationalUnitDN</span><span class="sxs-lookup"><span data-stu-id="fee89-126">-OrganizationalUnitDN</span></span>
<span data-ttu-id="fee89-127">Nazwa wyróżniająca jednostki organizacyjnej w usłudze Active Directory, w której zostaną utworzone konta użytkowników i komputerów</span><span class="sxs-lookup"><span data-stu-id="fee89-127">Distinguished name of the organizational unit in the Active directory where user and computer accounts will be created</span></span>

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

### <span data-ttu-id="fee89-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fee89-128">-Confirm</span></span>
<span data-ttu-id="fee89-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fee89-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fee89-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fee89-130">-WhatIf</span></span>
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

### <span data-ttu-id="fee89-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fee89-131">CommonParameters</span></span>
<span data-ttu-id="fee89-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fee89-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fee89-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fee89-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fee89-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fee89-134">INPUTS</span></span>

### <span data-ttu-id="fee89-135">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="fee89-135">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="fee89-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fee89-136">OUTPUTS</span></span>

### <span data-ttu-id="fee89-137">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="fee89-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile</span></span>

## <span data-ttu-id="fee89-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fee89-138">NOTES</span></span>

## <span data-ttu-id="fee89-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fee89-139">RELATED LINKS</span></span>
