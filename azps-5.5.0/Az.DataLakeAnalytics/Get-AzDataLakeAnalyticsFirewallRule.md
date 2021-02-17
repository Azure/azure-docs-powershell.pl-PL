---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 40c44ff157fca6a276cac8ece508e9d540b526ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186179"
---
# <span data-ttu-id="34462-101">Get-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="34462-101">Get-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="34462-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34462-102">SYNOPSIS</span></span>
<span data-ttu-id="34462-103">Pobiera regułę zapory lub listę reguł zapory z konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="34462-103">Retrieves a firewall rule or list of firewall rules from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="34462-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="34462-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34462-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="34462-105">DESCRIPTION</span></span>
<span data-ttu-id="34462-106">Polecenie **cmdlet Get-AzDataLakeAnalyticsFirewallRule** pobiera regułę zapory lub listę reguł zapory z konta usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="34462-106">The **Get-AzDataLakeAnalyticsFirewallRule** cmdlet retrieves a firewall rule or list of firewall rules from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="34462-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="34462-107">EXAMPLES</span></span>

### <span data-ttu-id="34462-108">Przykład 1. Uzyskiwanie reguły zapory</span><span class="sxs-lookup"><span data-stu-id="34462-108">Example 1: Get a firewall rule</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="34462-109">To polecenie pobiera regułę zapory o nazwie "moja reguła zapory" z konta "ContosoAdlAcct"</span><span class="sxs-lookup"><span data-stu-id="34462-109">This command gets the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

### <span data-ttu-id="34462-110">Przykład 2. Lista wszystkich reguł zapory</span><span class="sxs-lookup"><span data-stu-id="34462-110">Example 2: List all firewall rules</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct"
```

<span data-ttu-id="34462-111">To polecenie pobiera wszystkie reguły zapory z konta "ContosoAdlAcct"</span><span class="sxs-lookup"><span data-stu-id="34462-111">This command gets all firewall rules from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="34462-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34462-112">PARAMETERS</span></span>

### <span data-ttu-id="34462-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="34462-113">-Account</span></span>
<span data-ttu-id="34462-114">Konto Data Lake Analytics, z których można pobrać regułę zapory</span><span class="sxs-lookup"><span data-stu-id="34462-114">The Data Lake Analytics account to get the firewall rule from</span></span>

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

### <span data-ttu-id="34462-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34462-115">-DefaultProfile</span></span>
<span data-ttu-id="34462-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="34462-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34462-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="34462-117">-Name</span></span>
<span data-ttu-id="34462-118">Nazwa reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="34462-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="34462-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34462-119">-ResourceGroupName</span></span>
<span data-ttu-id="34462-120">Nazwa grupy zasobów, w ramach której chcesz pobrać konto.</span><span class="sxs-lookup"><span data-stu-id="34462-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="34462-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34462-121">CommonParameters</span></span>
<span data-ttu-id="34462-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34462-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34462-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34462-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34462-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34462-124">INPUTS</span></span>

### <span data-ttu-id="34462-125">System.String</span><span class="sxs-lookup"><span data-stu-id="34462-125">System.String</span></span>

## <span data-ttu-id="34462-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34462-126">OUTPUTS</span></span>

### <span data-ttu-id="34462-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="34462-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="34462-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="34462-128">NOTES</span></span>

## <span data-ttu-id="34462-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34462-129">RELATED LINKS</span></span>
