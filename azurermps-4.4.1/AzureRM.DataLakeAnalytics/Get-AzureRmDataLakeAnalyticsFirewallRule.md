---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 99acce24389a02c8fb50f5b313841319f813feaf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553933"
---
# <span data-ttu-id="ebf6d-101">Get-AzureRmDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ebf6d-101">Get-AzureRmDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="ebf6d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ebf6d-102">SYNOPSIS</span></span>
<span data-ttu-id="ebf6d-103">Pobiera regułę lub listę reguł zapory z konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="ebf6d-103">Retrieves a firewall rule or list of firewall rules from a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ebf6d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ebf6d-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ebf6d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ebf6d-105">DESCRIPTION</span></span>
<span data-ttu-id="ebf6d-106">Polecenie cmdlet **Get-AzureRmDataLakeAnalyticsFirewallRule** pobiera regułę lub listę reguł zapory z konta usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="ebf6d-106">The **Get-AzureRmDataLakeAnalyticsFirewallRule** cmdlet retrieves a firewall rule or list of firewall rules from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="ebf6d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ebf6d-107">EXAMPLES</span></span>

### <span data-ttu-id="ebf6d-108">Przykład 1: uzyskiwanie reguły zapory</span><span class="sxs-lookup"><span data-stu-id="ebf6d-108">Example 1: Get a firewall rule</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="ebf6d-109">To polecenie pobiera regułę zapory o nazwie "Moja Reguła zapory" z konta "ContosoAdlAcct"</span><span class="sxs-lookup"><span data-stu-id="ebf6d-109">This command gets the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

### <span data-ttu-id="ebf6d-110">Przykład 2: Lista wszystkich reguł zapory</span><span class="sxs-lookup"><span data-stu-id="ebf6d-110">Example 2: List all firewall rules</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct"
```

<span data-ttu-id="ebf6d-111">To polecenie pobiera wszystkie reguły zapory z konta "ContosoAdlAcct"</span><span class="sxs-lookup"><span data-stu-id="ebf6d-111">This command gets all firewall rules from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="ebf6d-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ebf6d-112">PARAMETERS</span></span>

### <span data-ttu-id="ebf6d-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="ebf6d-113">-Account</span></span>
<span data-ttu-id="ebf6d-114">Konto usługi Data Lake Analytics umożliwiające pobranie reguły zapory</span><span class="sxs-lookup"><span data-stu-id="ebf6d-114">The Data Lake Analytics account to get the firewall rule from</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebf6d-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ebf6d-115">-Name</span></span>
<span data-ttu-id="ebf6d-116">Nazwa reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="ebf6d-116">The name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebf6d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebf6d-117">-ResourceGroupName</span></span>
<span data-ttu-id="ebf6d-118">Nazwa grupy zasobów, pod którą ma zostać pobrane konto.</span><span class="sxs-lookup"><span data-stu-id="ebf6d-118">Name of resource group under which want to retrieve the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebf6d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebf6d-119">-DefaultProfile</span></span>
<span data-ttu-id="ebf6d-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ebf6d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ebf6d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebf6d-121">CommonParameters</span></span>
<span data-ttu-id="ebf6d-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebf6d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebf6d-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebf6d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebf6d-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ebf6d-124">INPUTS</span></span>

### <span data-ttu-id="ebf6d-125">System. String</span><span class="sxs-lookup"><span data-stu-id="ebf6d-125">System.String</span></span>

## <span data-ttu-id="ebf6d-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ebf6d-126">OUTPUTS</span></span>

### <span data-ttu-id="ebf6d-127">Microsoft. Azure. Commands. DataLakeAnalytics. models. DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ebf6d-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>
<span data-ttu-id="ebf6d-128">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. DataLakeAnalytics. MODELES. DataLakeAnalyticsFirewallRule, Microsoft. Azure. Commands</span><span class="sxs-lookup"><span data-stu-id="ebf6d-128">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule, Microsoft.Azure.Commands.DataLakeAnalytics, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ebf6d-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ebf6d-129">NOTES</span></span>

## <span data-ttu-id="ebf6d-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ebf6d-130">RELATED LINKS</span></span>
