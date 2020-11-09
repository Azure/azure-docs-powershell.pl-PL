---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 40c44ff157fca6a276cac8ece508e9d540b526ed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305850"
---
# <span data-ttu-id="6710c-101">Get-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6710c-101">Get-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="6710c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6710c-102">SYNOPSIS</span></span>
<span data-ttu-id="6710c-103">Pobiera regułę lub listę reguł zapory z konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6710c-103">Retrieves a firewall rule or list of firewall rules from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="6710c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6710c-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6710c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6710c-105">DESCRIPTION</span></span>
<span data-ttu-id="6710c-106">Polecenie cmdlet **Get-AzDataLakeAnalyticsFirewallRule** pobiera regułę lub listę reguł zapory z konta usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6710c-106">The **Get-AzDataLakeAnalyticsFirewallRule** cmdlet retrieves a firewall rule or list of firewall rules from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="6710c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6710c-107">EXAMPLES</span></span>

### <span data-ttu-id="6710c-108">Przykład 1: uzyskiwanie reguły zapory</span><span class="sxs-lookup"><span data-stu-id="6710c-108">Example 1: Get a firewall rule</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="6710c-109">To polecenie pobiera regułę zapory o nazwie "Moja Reguła zapory" z konta "ContosoAdlAcct"</span><span class="sxs-lookup"><span data-stu-id="6710c-109">This command gets the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

### <span data-ttu-id="6710c-110">Przykład 2: Lista wszystkich reguł zapory</span><span class="sxs-lookup"><span data-stu-id="6710c-110">Example 2: List all firewall rules</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct"
```

<span data-ttu-id="6710c-111">To polecenie pobiera wszystkie reguły zapory z konta "ContosoAdlAcct"</span><span class="sxs-lookup"><span data-stu-id="6710c-111">This command gets all firewall rules from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="6710c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6710c-112">PARAMETERS</span></span>

### <span data-ttu-id="6710c-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="6710c-113">-Account</span></span>
<span data-ttu-id="6710c-114">Konto usługi Data Lake Analytics umożliwiające pobranie reguły zapory</span><span class="sxs-lookup"><span data-stu-id="6710c-114">The Data Lake Analytics account to get the firewall rule from</span></span>

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

### <span data-ttu-id="6710c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6710c-115">-DefaultProfile</span></span>
<span data-ttu-id="6710c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="6710c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6710c-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6710c-117">-Name</span></span>
<span data-ttu-id="6710c-118">Nazwa reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="6710c-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="6710c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6710c-119">-ResourceGroupName</span></span>
<span data-ttu-id="6710c-120">Nazwa grupy zasobów, pod którą ma zostać pobrane konto.</span><span class="sxs-lookup"><span data-stu-id="6710c-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="6710c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6710c-121">CommonParameters</span></span>
<span data-ttu-id="6710c-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6710c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6710c-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6710c-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6710c-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6710c-124">INPUTS</span></span>

### <span data-ttu-id="6710c-125">System. String</span><span class="sxs-lookup"><span data-stu-id="6710c-125">System.String</span></span>

## <span data-ttu-id="6710c-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6710c-126">OUTPUTS</span></span>

### <span data-ttu-id="6710c-127">Microsoft. Azure. Commands. DataLakeAnalytics. models. DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6710c-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="6710c-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6710c-128">NOTES</span></span>

## <span data-ttu-id="6710c-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6710c-129">RELATED LINKS</span></span>
