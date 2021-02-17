---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 879897b6d89e5a1e34ee9f61714628aa741a670f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194787"
---
# <span data-ttu-id="d1d1f-101">Remove-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d1d1f-101">Remove-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="d1d1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1d1f-102">SYNOPSIS</span></span>
<span data-ttu-id="d1d1f-103">Usuwa regułę zapory z konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d1d1f-103">Removes a firewall rule from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="d1d1f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d1d1f-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d1d1f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d1d1f-105">DESCRIPTION</span></span>
<span data-ttu-id="d1d1f-106">Polecenie **cmdlet Remove-AzDataLakeAnalyticsFirewallRule** usuwa regułę zapory z konta usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d1d1f-106">The **Remove-AzDataLakeAnalyticsFirewallRule** cmdlet removes a firewall rule from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="d1d1f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d1d1f-107">EXAMPLES</span></span>

### <span data-ttu-id="d1d1f-108">Przykład 1. Usuwanie reguły zapory</span><span class="sxs-lookup"><span data-stu-id="d1d1f-108">Example 1: Remove a firewall rule</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="d1d1f-109">To polecenie usuwa regułę zapory o nazwie "moja reguła zapory" z konta "ContosoAdlAcct"</span><span class="sxs-lookup"><span data-stu-id="d1d1f-109">This command removes the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="d1d1f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1d1f-110">PARAMETERS</span></span>

### <span data-ttu-id="d1d1f-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="d1d1f-111">-Account</span></span>
<span data-ttu-id="d1d1f-112">Konto Data Lake Analytics w celu usunięcia reguły zapory z</span><span class="sxs-lookup"><span data-stu-id="d1d1f-112">The Data Lake Analytics account to remove the firewall rule from</span></span>

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

### <span data-ttu-id="d1d1f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1d1f-113">-DefaultProfile</span></span>
<span data-ttu-id="d1d1f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="d1d1f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d1d1f-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d1d1f-115">-Name</span></span>
<span data-ttu-id="d1d1f-116">Nazwa reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="d1d1f-116">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="d1d1f-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1d1f-117">-PassThru</span></span>
<span data-ttu-id="d1d1f-118">Wskazuje, że powinna zostać zwrócona odpowiedź logiczna wskazująca wynik operacji usuwania.</span><span class="sxs-lookup"><span data-stu-id="d1d1f-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="d1d1f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1d1f-119">-ResourceGroupName</span></span>
<span data-ttu-id="d1d1f-120">Nazwa grupy zasobów, w ramach której chcesz pobrać konto.</span><span class="sxs-lookup"><span data-stu-id="d1d1f-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="d1d1f-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d1d1f-121">-Confirm</span></span>
<span data-ttu-id="d1d1f-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d1d1f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1d1f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1d1f-123">-WhatIf</span></span>
<span data-ttu-id="d1d1f-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1d1f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1d1f-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d1d1f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1d1f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1d1f-126">CommonParameters</span></span>
<span data-ttu-id="d1d1f-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1d1f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1d1f-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1d1f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1d1f-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d1d1f-129">INPUTS</span></span>

### <span data-ttu-id="d1d1f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="d1d1f-130">System.String</span></span>

### <span data-ttu-id="d1d1f-131">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="d1d1f-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d1d1f-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d1d1f-132">OUTPUTS</span></span>

### <span data-ttu-id="d1d1f-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d1d1f-133">System.Boolean</span></span>

## <span data-ttu-id="d1d1f-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d1d1f-134">NOTES</span></span>

## <span data-ttu-id="d1d1f-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d1d1f-135">RELATED LINKS</span></span>
