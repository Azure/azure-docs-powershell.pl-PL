---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 6d179a4cc5814c45925802f606480927a3ed3af0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705865"
---
# <span data-ttu-id="ce3a9-101">Remove-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ce3a9-101">Remove-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="ce3a9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ce3a9-102">SYNOPSIS</span></span>
<span data-ttu-id="ce3a9-103">Usuwa regułę zapory z konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="ce3a9-103">Removes a firewall rule from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="ce3a9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ce3a9-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ce3a9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ce3a9-105">DESCRIPTION</span></span>
<span data-ttu-id="ce3a9-106">Polecenie cmdlet **Remove-AzDataLakeAnalyticsFirewallRule** usuwa regułę zapory z konta usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="ce3a9-106">The **Remove-AzDataLakeAnalyticsFirewallRule** cmdlet removes a firewall rule from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="ce3a9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ce3a9-107">EXAMPLES</span></span>

### <span data-ttu-id="ce3a9-108">Przykład 1: Usuwanie reguły zapory</span><span class="sxs-lookup"><span data-stu-id="ce3a9-108">Example 1: Remove a firewall rule</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="ce3a9-109">To polecenie usuwa regułę zapory o nazwie "Moja Reguła zapory" z konta "ContosoAdlAcct"</span><span class="sxs-lookup"><span data-stu-id="ce3a9-109">This command removes the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="ce3a9-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ce3a9-110">PARAMETERS</span></span>

### <span data-ttu-id="ce3a9-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="ce3a9-111">-Account</span></span>
<span data-ttu-id="ce3a9-112">Konto usługi Data Lake Analytics do usunięcia reguły zapory</span><span class="sxs-lookup"><span data-stu-id="ce3a9-112">The Data Lake Analytics account to remove the firewall rule from</span></span>

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

### <span data-ttu-id="ce3a9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce3a9-113">-DefaultProfile</span></span>
<span data-ttu-id="ce3a9-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ce3a9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce3a9-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ce3a9-115">-Name</span></span>
<span data-ttu-id="ce3a9-116">Nazwa reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="ce3a9-116">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="ce3a9-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce3a9-117">-PassThru</span></span>
<span data-ttu-id="ce3a9-118">Wskazuje, że należy zwrócić odpowiedź logiczną wskazującą wynik operacji usuwania.</span><span class="sxs-lookup"><span data-stu-id="ce3a9-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="ce3a9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce3a9-119">-ResourceGroupName</span></span>
<span data-ttu-id="ce3a9-120">Nazwa grupy zasobów, pod którą ma zostać pobrane konto.</span><span class="sxs-lookup"><span data-stu-id="ce3a9-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="ce3a9-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ce3a9-121">-Confirm</span></span>
<span data-ttu-id="ce3a9-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce3a9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce3a9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce3a9-123">-WhatIf</span></span>
<span data-ttu-id="ce3a9-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce3a9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce3a9-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ce3a9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce3a9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce3a9-126">CommonParameters</span></span>
<span data-ttu-id="ce3a9-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce3a9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce3a9-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce3a9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce3a9-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ce3a9-129">INPUTS</span></span>

### <span data-ttu-id="ce3a9-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ce3a9-130">System.String</span></span>

### <span data-ttu-id="ce3a9-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ce3a9-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ce3a9-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ce3a9-132">OUTPUTS</span></span>

### <span data-ttu-id="ce3a9-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ce3a9-133">System.Boolean</span></span>

## <span data-ttu-id="ce3a9-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ce3a9-134">NOTES</span></span>

## <span data-ttu-id="ce3a9-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ce3a9-135">RELATED LINKS</span></span>
