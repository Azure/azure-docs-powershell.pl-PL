---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 7D27F7B1-BAF8-4A01-8BA7-A75A4CFAE370
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: e8db3842997a5bd99b970921b31d66bbbc07007a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542640"
---
# <span data-ttu-id="f14fe-101">Get-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f14fe-101">Get-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="f14fe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f14fe-102">SYNOPSIS</span></span>
<span data-ttu-id="f14fe-103">Pobiera określone reguły zapory w określonym sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f14fe-103">Gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="f14fe-104">Jeśli nie określono żadnej reguły zapory, wyświetlane są wszystkie reguły zapory dla tego konta.</span><span class="sxs-lookup"><span data-stu-id="f14fe-104">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f14fe-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f14fe-105">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f14fe-106">Opis</span><span class="sxs-lookup"><span data-stu-id="f14fe-106">DESCRIPTION</span></span>
<span data-ttu-id="f14fe-107">Polecenie cmdlet Get-AzureRmDataLakeStoreFirewallRule pobiera określone reguły zapory w określonym sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f14fe-107">The Get-AzureRmDataLakeStoreFirewallRule cmdlet gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="f14fe-108">Jeśli nie określono żadnej reguły zapory, wyświetlane są wszystkie reguły zapory dla tego konta.</span><span class="sxs-lookup"><span data-stu-id="f14fe-108">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="f14fe-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f14fe-109">EXAMPLES</span></span>

### <span data-ttu-id="f14fe-110">Przykład 1: pobieranie określonej reguły zapory</span><span class="sxs-lookup"><span data-stu-id="f14fe-110">Example 1: Retrieve a specific firewall rule</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="f14fe-111">Zwraca regułę zapory o nazwie "MyFirewallRule" z konta "ContosoADL".</span><span class="sxs-lookup"><span data-stu-id="f14fe-111">Returns the firewall rule named "MyFirewallRule" from account "ContosoADL"</span></span>

### <span data-ttu-id="f14fe-112">Przykład 2: wyświetlanie wszystkich reguł zapory na koncie</span><span class="sxs-lookup"><span data-stu-id="f14fe-112">Example 2: List all firewall rules in an account</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL"
```

<span data-ttu-id="f14fe-113">Zwraca wszystkie reguły zapory na koncie "ContosoADL".</span><span class="sxs-lookup"><span data-stu-id="f14fe-113">Returns all firewall rules in account "ContosoADL"</span></span>

## <span data-ttu-id="f14fe-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f14fe-114">PARAMETERS</span></span>

### <span data-ttu-id="f14fe-115">— Konto</span><span class="sxs-lookup"><span data-stu-id="f14fe-115">-Account</span></span>
<span data-ttu-id="f14fe-116">Konto usługi Data Lake Store do pobierania reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="f14fe-116">The Data Lake Store account to retrieve the firewall rule from.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f14fe-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f14fe-117">-DefaultProfile</span></span>
<span data-ttu-id="f14fe-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f14fe-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f14fe-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f14fe-119">-Name</span></span>
<span data-ttu-id="f14fe-120">Nazwa reguły zapory do pobrania</span><span class="sxs-lookup"><span data-stu-id="f14fe-120">The name of the firewall rule to retrieve</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f14fe-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f14fe-121">-ResourceGroupName</span></span>
<span data-ttu-id="f14fe-122">Nazwa grupy zasobów, pod którą ma być pobierana określona Reguła zapory dla określonego konta.</span><span class="sxs-lookup"><span data-stu-id="f14fe-122">Name of resource group under which want to retrieve the specified account's specified firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f14fe-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f14fe-123">CommonParameters</span></span>
<span data-ttu-id="f14fe-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f14fe-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f14fe-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f14fe-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f14fe-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f14fe-126">INPUTS</span></span>

### <span data-ttu-id="f14fe-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f14fe-127">None</span></span>
<span data-ttu-id="f14fe-128">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="f14fe-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f14fe-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f14fe-129">OUTPUTS</span></span>

### <span data-ttu-id="f14fe-130">DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f14fe-130">DataLakeStoreFirewallRule</span></span>
<span data-ttu-id="f14fe-131">Określona Reguła zapory do pobrania</span><span class="sxs-lookup"><span data-stu-id="f14fe-131">The specified firewall rule to retrieve</span></span>

### <span data-ttu-id="f14fe-132">IList<DataLakeStoreFirewallRule></span><span class="sxs-lookup"><span data-stu-id="f14fe-132">IList<DataLakeStoreFirewallRule></span></span>
<span data-ttu-id="f14fe-133">Lista reguł zapory na określonym koncie.</span><span class="sxs-lookup"><span data-stu-id="f14fe-133">The list of firewall rules in the specified account.</span></span>

## <span data-ttu-id="f14fe-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f14fe-134">NOTES</span></span>

## <span data-ttu-id="f14fe-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f14fe-135">RELATED LINKS</span></span>

