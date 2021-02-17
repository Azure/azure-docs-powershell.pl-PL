---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 7D27F7B1-BAF8-4A01-8BA7-A75A4CFAE370
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: c681ba089487868b556bd6e0ae198384a0dadd8c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198147"
---
# <span data-ttu-id="0d7f8-101">Get-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0d7f8-101">Get-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="0d7f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d7f8-102">SYNOPSIS</span></span>
<span data-ttu-id="0d7f8-103">Pobiera określone reguły zapory w określonym magazynie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0d7f8-103">Gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="0d7f8-104">Jeśli nie zostanie określona żadna reguła zapory, zostanie wymieniona lista wszystkich reguł zapory dla konta.</span><span class="sxs-lookup"><span data-stu-id="0d7f8-104">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="0d7f8-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0d7f8-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d7f8-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="0d7f8-106">DESCRIPTION</span></span>
<span data-ttu-id="0d7f8-107">Polecenie Get-AzDataLakeStoreFirewallRule pobiera określone reguły zapory w określonym magazynie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0d7f8-107">The Get-AzDataLakeStoreFirewallRule cmdlet gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="0d7f8-108">Jeśli nie zostanie określona żadna reguła zapory, zostanie wymieniona lista wszystkich reguł zapory dla konta.</span><span class="sxs-lookup"><span data-stu-id="0d7f8-108">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="0d7f8-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0d7f8-109">EXAMPLES</span></span>

### <span data-ttu-id="0d7f8-110">Przykład 1. Pobieranie określonej reguły zapory</span><span class="sxs-lookup"><span data-stu-id="0d7f8-110">Example 1: Retrieve a specific firewall rule</span></span>
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="0d7f8-111">Zwraca regułę zapory o nazwie "MyFirewallRule" z konta "ContosoADL".</span><span class="sxs-lookup"><span data-stu-id="0d7f8-111">Returns the firewall rule named "MyFirewallRule" from account "ContosoADL"</span></span>

### <span data-ttu-id="0d7f8-112">Przykład 2. Lista wszystkich reguł zapory na koncie</span><span class="sxs-lookup"><span data-stu-id="0d7f8-112">Example 2: List all firewall rules in an account</span></span>
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL"
```

<span data-ttu-id="0d7f8-113">Zwraca wszystkie reguły zapory konta "ContosoADL".</span><span class="sxs-lookup"><span data-stu-id="0d7f8-113">Returns all firewall rules in account "ContosoADL"</span></span>

## <span data-ttu-id="0d7f8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0d7f8-114">PARAMETERS</span></span>

### <span data-ttu-id="0d7f8-115">— Konto</span><span class="sxs-lookup"><span data-stu-id="0d7f8-115">-Account</span></span>
<span data-ttu-id="0d7f8-116">Konto usługi Data Lake Store, z których jest pobierana reguła zapory.</span><span class="sxs-lookup"><span data-stu-id="0d7f8-116">The Data Lake Store account to retrieve the firewall rule from.</span></span>

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

### <span data-ttu-id="0d7f8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d7f8-117">-DefaultProfile</span></span>
<span data-ttu-id="0d7f8-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="0d7f8-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0d7f8-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0d7f8-119">-Name</span></span>
<span data-ttu-id="0d7f8-120">Nazwa reguły zapory do pobrania</span><span class="sxs-lookup"><span data-stu-id="0d7f8-120">The name of the firewall rule to retrieve</span></span>

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

### <span data-ttu-id="0d7f8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d7f8-121">-ResourceGroupName</span></span>
<span data-ttu-id="0d7f8-122">Nazwa grupy zasobów, w ramach której chcesz pobrać określoną regułę zapory dla określonego konta.</span><span class="sxs-lookup"><span data-stu-id="0d7f8-122">Name of resource group under which want to retrieve the specified account's specified firewall rule.</span></span>

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

### <span data-ttu-id="0d7f8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d7f8-123">CommonParameters</span></span>
<span data-ttu-id="0d7f8-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d7f8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d7f8-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d7f8-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d7f8-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0d7f8-126">INPUTS</span></span>

### <span data-ttu-id="0d7f8-127">System.String</span><span class="sxs-lookup"><span data-stu-id="0d7f8-127">System.String</span></span>

## <span data-ttu-id="0d7f8-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0d7f8-128">OUTPUTS</span></span>

### <span data-ttu-id="0d7f8-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0d7f8-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="0d7f8-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0d7f8-130">NOTES</span></span>

## <span data-ttu-id="0d7f8-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0d7f8-131">RELATED LINKS</span></span>
