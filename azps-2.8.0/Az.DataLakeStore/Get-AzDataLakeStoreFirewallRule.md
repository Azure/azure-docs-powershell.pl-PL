---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 7D27F7B1-BAF8-4A01-8BA7-A75A4CFAE370
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: 39450f979a4c79e453c66845b522aba91757f672
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705814"
---
# <span data-ttu-id="a1872-101">Get-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a1872-101">Get-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="a1872-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a1872-102">SYNOPSIS</span></span>
<span data-ttu-id="a1872-103">Pobiera określone reguły zapory w określonym sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a1872-103">Gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="a1872-104">Jeśli nie określono żadnej reguły zapory, wyświetlane są wszystkie reguły zapory dla tego konta.</span><span class="sxs-lookup"><span data-stu-id="a1872-104">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="a1872-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a1872-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1872-106">Opis</span><span class="sxs-lookup"><span data-stu-id="a1872-106">DESCRIPTION</span></span>
<span data-ttu-id="a1872-107">Polecenie cmdlet Get-AzDataLakeStoreFirewallRule pobiera określone reguły zapory w określonym sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a1872-107">The Get-AzDataLakeStoreFirewallRule cmdlet gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="a1872-108">Jeśli nie określono żadnej reguły zapory, wyświetlane są wszystkie reguły zapory dla tego konta.</span><span class="sxs-lookup"><span data-stu-id="a1872-108">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="a1872-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a1872-109">EXAMPLES</span></span>

### <span data-ttu-id="a1872-110">Przykład 1: pobieranie określonej reguły zapory</span><span class="sxs-lookup"><span data-stu-id="a1872-110">Example 1: Retrieve a specific firewall rule</span></span>
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="a1872-111">Zwraca regułę zapory o nazwie "MyFirewallRule" z konta "ContosoADL".</span><span class="sxs-lookup"><span data-stu-id="a1872-111">Returns the firewall rule named "MyFirewallRule" from account "ContosoADL"</span></span>

### <span data-ttu-id="a1872-112">Przykład 2: wyświetlanie wszystkich reguł zapory na koncie</span><span class="sxs-lookup"><span data-stu-id="a1872-112">Example 2: List all firewall rules in an account</span></span>
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL"
```

<span data-ttu-id="a1872-113">Zwraca wszystkie reguły zapory na koncie "ContosoADL".</span><span class="sxs-lookup"><span data-stu-id="a1872-113">Returns all firewall rules in account "ContosoADL"</span></span>

## <span data-ttu-id="a1872-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a1872-114">PARAMETERS</span></span>

### <span data-ttu-id="a1872-115">— Konto</span><span class="sxs-lookup"><span data-stu-id="a1872-115">-Account</span></span>
<span data-ttu-id="a1872-116">Konto usługi Data Lake Store do pobierania reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="a1872-116">The Data Lake Store account to retrieve the firewall rule from.</span></span>

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

### <span data-ttu-id="a1872-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1872-117">-DefaultProfile</span></span>
<span data-ttu-id="a1872-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a1872-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a1872-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a1872-119">-Name</span></span>
<span data-ttu-id="a1872-120">Nazwa reguły zapory do pobrania</span><span class="sxs-lookup"><span data-stu-id="a1872-120">The name of the firewall rule to retrieve</span></span>

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

### <span data-ttu-id="a1872-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1872-121">-ResourceGroupName</span></span>
<span data-ttu-id="a1872-122">Nazwa grupy zasobów, pod którą ma być pobierana określona Reguła zapory dla określonego konta.</span><span class="sxs-lookup"><span data-stu-id="a1872-122">Name of resource group under which want to retrieve the specified account's specified firewall rule.</span></span>

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

### <span data-ttu-id="a1872-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1872-123">CommonParameters</span></span>
<span data-ttu-id="a1872-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1872-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1872-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1872-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1872-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1872-126">INPUTS</span></span>

### <span data-ttu-id="a1872-127">System. String</span><span class="sxs-lookup"><span data-stu-id="a1872-127">System.String</span></span>

## <span data-ttu-id="a1872-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a1872-128">OUTPUTS</span></span>

### <span data-ttu-id="a1872-129">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a1872-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="a1872-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a1872-130">NOTES</span></span>

## <span data-ttu-id="a1872-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a1872-131">RELATED LINKS</span></span>