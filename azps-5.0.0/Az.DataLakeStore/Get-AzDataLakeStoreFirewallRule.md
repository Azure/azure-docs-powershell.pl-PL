---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 7D27F7B1-BAF8-4A01-8BA7-A75A4CFAE370
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: c681ba089487868b556bd6e0ae198384a0dadd8c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305622"
---
# <span data-ttu-id="92533-101">Get-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="92533-101">Get-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="92533-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="92533-102">SYNOPSIS</span></span>
<span data-ttu-id="92533-103">Pobiera określone reguły zapory w określonym sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="92533-103">Gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="92533-104">Jeśli nie określono żadnej reguły zapory, wyświetlane są wszystkie reguły zapory dla tego konta.</span><span class="sxs-lookup"><span data-stu-id="92533-104">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="92533-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="92533-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92533-106">Opis</span><span class="sxs-lookup"><span data-stu-id="92533-106">DESCRIPTION</span></span>
<span data-ttu-id="92533-107">Polecenie cmdlet Get-AzDataLakeStoreFirewallRule pobiera określone reguły zapory w określonym sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="92533-107">The Get-AzDataLakeStoreFirewallRule cmdlet gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="92533-108">Jeśli nie określono żadnej reguły zapory, wyświetlane są wszystkie reguły zapory dla tego konta.</span><span class="sxs-lookup"><span data-stu-id="92533-108">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="92533-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="92533-109">EXAMPLES</span></span>

### <span data-ttu-id="92533-110">Przykład 1: pobieranie określonej reguły zapory</span><span class="sxs-lookup"><span data-stu-id="92533-110">Example 1: Retrieve a specific firewall rule</span></span>
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="92533-111">Zwraca regułę zapory o nazwie "MyFirewallRule" z konta "ContosoADL".</span><span class="sxs-lookup"><span data-stu-id="92533-111">Returns the firewall rule named "MyFirewallRule" from account "ContosoADL"</span></span>

### <span data-ttu-id="92533-112">Przykład 2: wyświetlanie wszystkich reguł zapory na koncie</span><span class="sxs-lookup"><span data-stu-id="92533-112">Example 2: List all firewall rules in an account</span></span>
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL"
```

<span data-ttu-id="92533-113">Zwraca wszystkie reguły zapory na koncie "ContosoADL".</span><span class="sxs-lookup"><span data-stu-id="92533-113">Returns all firewall rules in account "ContosoADL"</span></span>

## <span data-ttu-id="92533-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="92533-114">PARAMETERS</span></span>

### <span data-ttu-id="92533-115">— Konto</span><span class="sxs-lookup"><span data-stu-id="92533-115">-Account</span></span>
<span data-ttu-id="92533-116">Konto usługi Data Lake Store do pobierania reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="92533-116">The Data Lake Store account to retrieve the firewall rule from.</span></span>

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

### <span data-ttu-id="92533-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92533-117">-DefaultProfile</span></span>
<span data-ttu-id="92533-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="92533-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="92533-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="92533-119">-Name</span></span>
<span data-ttu-id="92533-120">Nazwa reguły zapory do pobrania</span><span class="sxs-lookup"><span data-stu-id="92533-120">The name of the firewall rule to retrieve</span></span>

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

### <span data-ttu-id="92533-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92533-121">-ResourceGroupName</span></span>
<span data-ttu-id="92533-122">Nazwa grupy zasobów, pod którą ma być pobierana określona Reguła zapory dla określonego konta.</span><span class="sxs-lookup"><span data-stu-id="92533-122">Name of resource group under which want to retrieve the specified account's specified firewall rule.</span></span>

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

### <span data-ttu-id="92533-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92533-123">CommonParameters</span></span>
<span data-ttu-id="92533-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92533-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92533-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92533-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92533-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="92533-126">INPUTS</span></span>

### <span data-ttu-id="92533-127">System. String</span><span class="sxs-lookup"><span data-stu-id="92533-127">System.String</span></span>

## <span data-ttu-id="92533-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="92533-128">OUTPUTS</span></span>

### <span data-ttu-id="92533-129">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="92533-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="92533-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="92533-130">NOTES</span></span>

## <span data-ttu-id="92533-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="92533-131">RELATED LINKS</span></span>
