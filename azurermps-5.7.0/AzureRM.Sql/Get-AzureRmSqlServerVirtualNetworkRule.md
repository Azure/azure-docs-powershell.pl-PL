---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 14eb3de52c08c276638c5079a1e64c65da6669f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551488"
---
# <span data-ttu-id="f2908-101">Get-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f2908-101">Get-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="f2908-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f2908-102">SYNOPSIS</span></span>
<span data-ttu-id="f2908-103">Pobiera lub wyświetla regułę wirtualnej sieci programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f2908-103">Gets or lists Azure SQL Server Virtual Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2908-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f2908-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerVirtualNetworkRule [-VirtualNetworkRuleName <String>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2908-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f2908-105">DESCRIPTION</span></span>
<span data-ttu-id="f2908-106">To polecenie pobiera określoną regułę sieci wirtualnej usługi Azure SQL Server lub listę reguł wirtualnej sieci usługi Azure SQL Server w obszarze serwera.</span><span class="sxs-lookup"><span data-stu-id="f2908-106">This command gets a specific Azure SQL Server Virtual Network Rule or a list of Azure SQL Server Virtual Network Rules under a server.</span></span>

## <span data-ttu-id="f2908-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f2908-107">EXAMPLES</span></span>

### <span data-ttu-id="f2908-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f2908-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Get-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="f2908-109">Pobiera pojedynczą regułę sieci wirtualnej usługi Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="f2908-109">Gets an single Azure SQL Server virtual network rule</span></span>

### <span data-ttu-id="f2908-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f2908-110">Example 2</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName
```

<span data-ttu-id="f2908-111">Pobiera listę reguł wirtualnej sieci programu Azure SQL Server w ramach określonego serwera.</span><span class="sxs-lookup"><span data-stu-id="f2908-111">Gets the list of Azure SQL Server virtual network rules under the specified server</span></span>

## <span data-ttu-id="f2908-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f2908-112">PARAMETERS</span></span>

### <span data-ttu-id="f2908-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2908-113">-DefaultProfile</span></span>
<span data-ttu-id="f2908-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f2908-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2908-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2908-115">-ResourceGroupName</span></span>
<span data-ttu-id="f2908-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f2908-116">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2908-117">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="f2908-117">-ServerName</span></span>
<span data-ttu-id="f2908-118">Nazwa programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f2908-118">The Azure Sql Server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2908-119">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="f2908-119">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="f2908-120">Nazwa reguły sieci wirtualnej platformy Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f2908-120">The Azure Sql Server Virtual Network Rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2908-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2908-121">CommonParameters</span></span>
<span data-ttu-id="f2908-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2908-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2908-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2908-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2908-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2908-124">INPUTS</span></span>

### <span data-ttu-id="f2908-125">System. String</span><span class="sxs-lookup"><span data-stu-id="f2908-125">System.String</span></span>

## <span data-ttu-id="f2908-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f2908-126">OUTPUTS</span></span>

### <span data-ttu-id="f2908-127">Microsoft. Azure. Commands. SQL. VirtualNetworkRule. model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="f2908-127">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="f2908-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f2908-128">NOTES</span></span>

## <span data-ttu-id="f2908-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f2908-129">RELATED LINKS</span></span>
