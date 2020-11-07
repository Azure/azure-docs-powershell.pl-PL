---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 239e9325532b18140a36e4b8f9a8f291e508a91c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541743"
---
# <span data-ttu-id="0accc-101">Remove-AzureRmDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0accc-101">Remove-AzureRmDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="0accc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0accc-102">SYNOPSIS</span></span>
<span data-ttu-id="0accc-103">Usuwa regułę zapory z konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="0accc-103">Removes a firewall rule from a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0accc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0accc-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0accc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0accc-105">DESCRIPTION</span></span>
<span data-ttu-id="0accc-106">Polecenie cmdlet **Remove-AzureRmDataLakeAnalyticsFirewallRule** usuwa regułę zapory z konta usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="0accc-106">The **Remove-AzureRmDataLakeAnalyticsFirewallRule** cmdlet removes a firewall rule from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="0accc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0accc-107">EXAMPLES</span></span>

### <span data-ttu-id="0accc-108">Przykład 1: Usuwanie reguły zapory</span><span class="sxs-lookup"><span data-stu-id="0accc-108">Example 1: Remove a firewall rule</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="0accc-109">To polecenie usuwa regułę zapory o nazwie "Moja Reguła zapory" z konta "ContosoAdlAcct"</span><span class="sxs-lookup"><span data-stu-id="0accc-109">This command removes the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="0accc-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0accc-110">PARAMETERS</span></span>

### <span data-ttu-id="0accc-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="0accc-111">-Account</span></span>
<span data-ttu-id="0accc-112">Konto usługi Data Lake Analytics do usunięcia reguły zapory</span><span class="sxs-lookup"><span data-stu-id="0accc-112">The Data Lake Analytics account to remove the firewall rule from</span></span>

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

### <span data-ttu-id="0accc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0accc-113">-DefaultProfile</span></span>
<span data-ttu-id="0accc-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="0accc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0accc-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0accc-115">-Name</span></span>
<span data-ttu-id="0accc-116">Nazwa reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="0accc-116">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="0accc-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0accc-117">-PassThru</span></span>
<span data-ttu-id="0accc-118">Wskazuje, że należy zwrócić odpowiedź logiczną wskazującą wynik operacji usuwania.</span><span class="sxs-lookup"><span data-stu-id="0accc-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0accc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0accc-119">-ResourceGroupName</span></span>
<span data-ttu-id="0accc-120">Nazwa grupy zasobów, pod którą ma zostać pobrane konto.</span><span class="sxs-lookup"><span data-stu-id="0accc-120">Name of resource group under which want to retrieve the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0accc-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0accc-121">-Confirm</span></span>
<span data-ttu-id="0accc-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0accc-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0accc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0accc-123">-WhatIf</span></span>
<span data-ttu-id="0accc-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0accc-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0accc-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0accc-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0accc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0accc-126">CommonParameters</span></span>
<span data-ttu-id="0accc-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0accc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0accc-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0accc-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0accc-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0accc-129">INPUTS</span></span>

### <span data-ttu-id="0accc-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0accc-130">System.String</span></span>

### <span data-ttu-id="0accc-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0accc-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0accc-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0accc-132">OUTPUTS</span></span>

### <span data-ttu-id="0accc-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0accc-133">System.Boolean</span></span>

## <span data-ttu-id="0accc-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0accc-134">NOTES</span></span>

## <span data-ttu-id="0accc-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0accc-135">RELATED LINKS</span></span>