---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: FB37494B-4035-45B7-88AB-DF33CEEF0D0A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightSecurityProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightSecurityProfile.md
ms.openlocfilehash: 7ea9f9d9bb07cae6db62c51b9d496f7117eee700
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551879"
---
# <span data-ttu-id="73baf-101">Add-AzureRmHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="73baf-101">Add-AzureRmHDInsightSecurityProfile</span></span>

## <span data-ttu-id="73baf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="73baf-102">SYNOPSIS</span></span>
<span data-ttu-id="73baf-103">Dodaje profileto zabezpieczeń do obiektu konfiguracji klastra.</span><span class="sxs-lookup"><span data-stu-id="73baf-103">Adds a security profileto a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73baf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="73baf-104">SYNTAX</span></span>

```
Add-AzureRmHDInsightSecurityProfile [-Config] <AzureHDInsightConfig> -Domain <String>
 -DomainUserCredential <PSCredential> -OrganizationalUnitDN <String> -LdapsUrls <String[]>
 [-ClusterUsersGroupDNs <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="73baf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="73baf-105">DESCRIPTION</span></span>
<span data-ttu-id="73baf-106">Profil zabezpieczeń służy do tworzenia bezpiecznego klastra przez kerberizing go.</span><span class="sxs-lookup"><span data-stu-id="73baf-106">Security profile is used to create a secure cluster by kerberizing it.</span></span>
<span data-ttu-id="73baf-107">Profil zabezpieczeń zawiera konfigurację powiązana z dołączeniem klastra do domeny usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="73baf-107">Security profile contains configuration related joining the cluster to Active Directory Domain.</span></span>

## <span data-ttu-id="73baf-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="73baf-108">EXAMPLES</span></span>

### <span data-ttu-id="73baf-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="73baf-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="73baf-110">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="73baf-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="73baf-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="73baf-111">PARAMETERS</span></span>

### <span data-ttu-id="73baf-112">-ClusterUsersGroupDNs</span><span class="sxs-lookup"><span data-stu-id="73baf-112">-ClusterUsersGroupDNs</span></span>
<span data-ttu-id="73baf-113">Nazwy wyróżniające grup usługi Active Directory, które będą dostępne w Ambari i Ranger</span><span class="sxs-lookup"><span data-stu-id="73baf-113">Distinguished names of the Active Directory groups that will be available in Ambari and Ranger</span></span>

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

### <span data-ttu-id="73baf-114">-Config</span><span class="sxs-lookup"><span data-stu-id="73baf-114">-Config</span></span>
<span data-ttu-id="73baf-115">Określa obiekt konfiguracji klastra usługi HDInsight, który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73baf-115">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="73baf-116">Ten obiekt jest tworzony za pomocą polecenia cmdlet New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="73baf-116">This object is created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="73baf-117">-Domain</span><span class="sxs-lookup"><span data-stu-id="73baf-117">-Domain</span></span>
<span data-ttu-id="73baf-118">Domena usługi Active Directory dla klastra</span><span class="sxs-lookup"><span data-stu-id="73baf-118">Active Directory domain for the cluster</span></span>

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

### <span data-ttu-id="73baf-119">-DomainUserCredential</span><span class="sxs-lookup"><span data-stu-id="73baf-119">-DomainUserCredential</span></span>
<span data-ttu-id="73baf-120">Poświadczenia konta użytkownika domeny z odpowiednimi uprawnieniami do tworzenia klastra.</span><span class="sxs-lookup"><span data-stu-id="73baf-120">A domain user account credential with sufficient permissions for creating the cluster.</span></span>
<span data-ttu-id="73baf-121">Nazwa użytkownika powinna być w user@domain formacie</span><span class="sxs-lookup"><span data-stu-id="73baf-121">Username should be in user@domain format</span></span>

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

### <span data-ttu-id="73baf-122">-LdapsUrls</span><span class="sxs-lookup"><span data-stu-id="73baf-122">-LdapsUrls</span></span>
<span data-ttu-id="73baf-123">Adresy URL jednego lub wielu serwerów LDAP dla usługi Active Directory</span><span class="sxs-lookup"><span data-stu-id="73baf-123">Urls of one or multiple LDAPS servers for the Active Directory</span></span>

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

### <span data-ttu-id="73baf-124">-OrganizationalUnitDN</span><span class="sxs-lookup"><span data-stu-id="73baf-124">-OrganizationalUnitDN</span></span>
<span data-ttu-id="73baf-125">Nazwa wyróżniająca jednostki organizacyjnej w usłudze Active Directory, w której zostaną utworzone konta użytkowników i komputerów</span><span class="sxs-lookup"><span data-stu-id="73baf-125">Distinguished name of the organizational unit in the Active directory where user and computer accounts will be created</span></span>

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

### <span data-ttu-id="73baf-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="73baf-126">-Confirm</span></span>
<span data-ttu-id="73baf-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73baf-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73baf-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73baf-128">-WhatIf</span></span>
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

### <span data-ttu-id="73baf-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73baf-129">-DefaultProfile</span></span>
<span data-ttu-id="73baf-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="73baf-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73baf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73baf-131">CommonParameters</span></span>
<span data-ttu-id="73baf-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73baf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73baf-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73baf-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73baf-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="73baf-134">INPUTS</span></span>

### <span data-ttu-id="73baf-135">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="73baf-135">AzureHDInsightConfig</span></span>
<span data-ttu-id="73baf-136">Parametr "config" akceptuje wartość typu "AzureHDInsightConfig" z procesu</span><span class="sxs-lookup"><span data-stu-id="73baf-136">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="73baf-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="73baf-137">OUTPUTS</span></span>

### <span data-ttu-id="73baf-138">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="73baf-138">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile</span></span>

## <span data-ttu-id="73baf-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="73baf-139">NOTES</span></span>

## <span data-ttu-id="73baf-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="73baf-140">RELATED LINKS</span></span>

