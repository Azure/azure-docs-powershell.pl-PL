---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: FB37494B-4035-45B7-88AB-DF33CEEF0D0A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/add-azurermhdinsightsecurityprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightSecurityProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightSecurityProfile.md
ms.openlocfilehash: 003072e6821561c78975d50fa627edf0f7fd120a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545323"
---
# <span data-ttu-id="2f9cb-101">Add-AzureRmHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="2f9cb-101">Add-AzureRmHDInsightSecurityProfile</span></span>

## <span data-ttu-id="2f9cb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2f9cb-102">SYNOPSIS</span></span>
<span data-ttu-id="2f9cb-103">Dodaje profileto zabezpieczeń do obiektu konfiguracji klastra.</span><span class="sxs-lookup"><span data-stu-id="2f9cb-103">Adds a security profileto a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f9cb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2f9cb-104">SYNTAX</span></span>

```
Add-AzureRmHDInsightSecurityProfile [-Config] <AzureHDInsightConfig> -Domain <String>
 -DomainUserCredential <PSCredential> -OrganizationalUnitDN <String> -LdapsUrls <String[]>
 [-ClusterUsersGroupDNs <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2f9cb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2f9cb-105">DESCRIPTION</span></span>
<span data-ttu-id="2f9cb-106">Profil zabezpieczeń służy do tworzenia bezpiecznego klastra przez kerberizing go.</span><span class="sxs-lookup"><span data-stu-id="2f9cb-106">Security profile is used to create a secure cluster by kerberizing it.</span></span>
<span data-ttu-id="2f9cb-107">Profil zabezpieczeń zawiera konfigurację powiązana z dołączeniem klastra do domeny usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2f9cb-107">Security profile contains configuration related joining the cluster to Active Directory Domain.</span></span>

## <span data-ttu-id="2f9cb-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2f9cb-108">EXAMPLES</span></span>

### <span data-ttu-id="2f9cb-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2f9cb-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="2f9cb-110">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="2f9cb-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="2f9cb-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2f9cb-111">PARAMETERS</span></span>

### <span data-ttu-id="2f9cb-112">-ClusterUsersGroupDNs</span><span class="sxs-lookup"><span data-stu-id="2f9cb-112">-ClusterUsersGroupDNs</span></span>
<span data-ttu-id="2f9cb-113">Nazwy wyróżniające grup usługi Active Directory, które będą dostępne w Ambari i Ranger</span><span class="sxs-lookup"><span data-stu-id="2f9cb-113">Distinguished names of the Active Directory groups that will be available in Ambari and Ranger</span></span>

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

### <span data-ttu-id="2f9cb-114">-Config</span><span class="sxs-lookup"><span data-stu-id="2f9cb-114">-Config</span></span>
<span data-ttu-id="2f9cb-115">Określa obiekt konfiguracji klastra usługi HDInsight, który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f9cb-115">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="2f9cb-116">Ten obiekt jest tworzony za pomocą polecenia cmdlet New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="2f9cb-116">This object is created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="2f9cb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f9cb-117">-DefaultProfile</span></span>
<span data-ttu-id="2f9cb-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="2f9cb-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2f9cb-119">-Domain</span><span class="sxs-lookup"><span data-stu-id="2f9cb-119">-Domain</span></span>
<span data-ttu-id="2f9cb-120">Domena usługi Active Directory dla klastra</span><span class="sxs-lookup"><span data-stu-id="2f9cb-120">Active Directory domain for the cluster</span></span>

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

### <span data-ttu-id="2f9cb-121">-DomainUserCredential</span><span class="sxs-lookup"><span data-stu-id="2f9cb-121">-DomainUserCredential</span></span>
<span data-ttu-id="2f9cb-122">Poświadczenia konta użytkownika domeny z odpowiednimi uprawnieniami do tworzenia klastra.</span><span class="sxs-lookup"><span data-stu-id="2f9cb-122">A domain user account credential with sufficient permissions for creating the cluster.</span></span>
<span data-ttu-id="2f9cb-123">Nazwa użytkownika powinna być w user@domain formacie</span><span class="sxs-lookup"><span data-stu-id="2f9cb-123">Username should be in user@domain format</span></span>

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

### <span data-ttu-id="2f9cb-124">-LdapsUrls</span><span class="sxs-lookup"><span data-stu-id="2f9cb-124">-LdapsUrls</span></span>
<span data-ttu-id="2f9cb-125">Adresy URL jednego lub wielu serwerów LDAP dla usługi Active Directory</span><span class="sxs-lookup"><span data-stu-id="2f9cb-125">Urls of one or multiple LDAPS servers for the Active Directory</span></span>

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

### <span data-ttu-id="2f9cb-126">-OrganizationalUnitDN</span><span class="sxs-lookup"><span data-stu-id="2f9cb-126">-OrganizationalUnitDN</span></span>
<span data-ttu-id="2f9cb-127">Nazwa wyróżniająca jednostki organizacyjnej w usłudze Active Directory, w której zostaną utworzone konta użytkowników i komputerów</span><span class="sxs-lookup"><span data-stu-id="2f9cb-127">Distinguished name of the organizational unit in the Active directory where user and computer accounts will be created</span></span>

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

### <span data-ttu-id="2f9cb-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2f9cb-128">-Confirm</span></span>
<span data-ttu-id="2f9cb-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f9cb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f9cb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f9cb-130">-WhatIf</span></span>
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

### <span data-ttu-id="2f9cb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f9cb-131">CommonParameters</span></span>
<span data-ttu-id="2f9cb-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f9cb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f9cb-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f9cb-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f9cb-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2f9cb-134">INPUTS</span></span>

### <span data-ttu-id="2f9cb-135">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="2f9cb-135">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>
<span data-ttu-id="2f9cb-136">Parametry: config (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2f9cb-136">Parameters: Config (ByValue)</span></span>

## <span data-ttu-id="2f9cb-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2f9cb-137">OUTPUTS</span></span>

### <span data-ttu-id="2f9cb-138">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="2f9cb-138">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile</span></span>

## <span data-ttu-id="2f9cb-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2f9cb-139">NOTES</span></span>

## <span data-ttu-id="2f9cb-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2f9cb-140">RELATED LINKS</span></span>
