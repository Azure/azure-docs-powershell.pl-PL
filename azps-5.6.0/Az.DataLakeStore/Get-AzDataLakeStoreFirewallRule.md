---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 7D27F7B1-BAF8-4A01-8BA7-A75A4CFAE370
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: 580b5518e1fc0894a51920e781464258bef9e9cc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966666"
---
# <span data-ttu-id="f10af-101">Get-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f10af-101">Get-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="f10af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f10af-102">SYNOPSIS</span></span>
<span data-ttu-id="f10af-103">Pobiera określone reguły zapory w określonym magazynie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f10af-103">Gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="f10af-104">Jeśli nie zostanie określona żadna reguła zapory, zostanie wymieniona lista wszystkich reguł zapory dla konta.</span><span class="sxs-lookup"><span data-stu-id="f10af-104">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="f10af-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f10af-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f10af-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="f10af-106">DESCRIPTION</span></span>
<span data-ttu-id="f10af-107">Polecenie Get-AzDataLakeStoreFirewallRule pobiera określone reguły zapory w określonym magazynie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f10af-107">The Get-AzDataLakeStoreFirewallRule cmdlet gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="f10af-108">Jeśli nie zostanie określona żadna reguła zapory, zostanie wymieniona lista wszystkich reguł zapory dla konta.</span><span class="sxs-lookup"><span data-stu-id="f10af-108">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="f10af-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f10af-109">EXAMPLES</span></span>

### <span data-ttu-id="f10af-110">Przykład 1. Pobieranie określonej reguły zapory</span><span class="sxs-lookup"><span data-stu-id="f10af-110">Example 1: Retrieve a specific firewall rule</span></span>
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="f10af-111">Zwraca regułę zapory o nazwie "MyFirewallRule" z konta "ContosoADL".</span><span class="sxs-lookup"><span data-stu-id="f10af-111">Returns the firewall rule named "MyFirewallRule" from account "ContosoADL"</span></span>

### <span data-ttu-id="f10af-112">Przykład 2. Lista wszystkich reguł zapory na koncie</span><span class="sxs-lookup"><span data-stu-id="f10af-112">Example 2: List all firewall rules in an account</span></span>
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL"
```

<span data-ttu-id="f10af-113">Zwraca wszystkie reguły zapory konta "ContosoADL".</span><span class="sxs-lookup"><span data-stu-id="f10af-113">Returns all firewall rules in account "ContosoADL"</span></span>

## <span data-ttu-id="f10af-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f10af-114">PARAMETERS</span></span>

### <span data-ttu-id="f10af-115">— Konto</span><span class="sxs-lookup"><span data-stu-id="f10af-115">-Account</span></span>
<span data-ttu-id="f10af-116">Konto usługi Data Lake Store, z których jest pobierana reguła zapory.</span><span class="sxs-lookup"><span data-stu-id="f10af-116">The Data Lake Store account to retrieve the firewall rule from.</span></span>

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

### <span data-ttu-id="f10af-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f10af-117">-DefaultProfile</span></span>
<span data-ttu-id="f10af-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="f10af-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f10af-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f10af-119">-Name</span></span>
<span data-ttu-id="f10af-120">Nazwa reguły zapory do pobrania</span><span class="sxs-lookup"><span data-stu-id="f10af-120">The name of the firewall rule to retrieve</span></span>

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

### <span data-ttu-id="f10af-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f10af-121">-ResourceGroupName</span></span>
<span data-ttu-id="f10af-122">Nazwa grupy zasobów, w ramach której chcesz pobrać określoną regułę zapory dla określonego konta.</span><span class="sxs-lookup"><span data-stu-id="f10af-122">Name of resource group under which want to retrieve the specified account's specified firewall rule.</span></span>

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

### <span data-ttu-id="f10af-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f10af-123">CommonParameters</span></span>
<span data-ttu-id="f10af-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f10af-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f10af-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f10af-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f10af-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f10af-126">INPUTS</span></span>

### <span data-ttu-id="f10af-127">System.String</span><span class="sxs-lookup"><span data-stu-id="f10af-127">System.String</span></span>

## <span data-ttu-id="f10af-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f10af-128">OUTPUTS</span></span>

### <span data-ttu-id="f10af-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f10af-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="f10af-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f10af-130">NOTES</span></span>

## <span data-ttu-id="f10af-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f10af-131">RELATED LINKS</span></span>
