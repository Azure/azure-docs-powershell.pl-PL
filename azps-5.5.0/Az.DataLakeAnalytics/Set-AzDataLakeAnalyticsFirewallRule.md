---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 91941fbef7363a56da8a8021294750cc862aab55
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194739"
---
# <span data-ttu-id="7ad5a-101">Set-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7ad5a-101">Set-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="7ad5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ad5a-102">SYNOPSIS</span></span>
<span data-ttu-id="7ad5a-103">Aktualizuje regułę zapory na koncie usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="7ad5a-103">Updates a firewall rule in a Data Lake Analytics account.</span></span>

## <span data-ttu-id="7ad5a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7ad5a-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ad5a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="7ad5a-105">DESCRIPTION</span></span>
<span data-ttu-id="7ad5a-106">Polecenie **cmdlet Set-AzDataLakeAnalyticsFirewallRule** aktualizuje regułę zapory na koncie usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="7ad5a-106">The **Set-AzDataLakeAnalyticsFirewallRule** cmdlet updates a firewall rule in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="7ad5a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7ad5a-107">EXAMPLES</span></span>

### <span data-ttu-id="7ad5a-108">Przykład 1. Aktualizowanie reguły zapory</span><span class="sxs-lookup"><span data-stu-id="7ad5a-108">Example 1: Update a firewall rule</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="7ad5a-109">To polecenie aktualizuje regułę zapory o nazwie "reguła mojej zapory" w koncie "ContosoAdlAcct", aby nowy zakres adresów IP: 127.0.0.1 – 127.0.0.10</span><span class="sxs-lookup"><span data-stu-id="7ad5a-109">This command updates the firewall rule named "my firewall rule" in account "ContosoAdlAcct" to have the new IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="7ad5a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ad5a-110">PARAMETERS</span></span>

### <span data-ttu-id="7ad5a-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="7ad5a-111">-Account</span></span>
<span data-ttu-id="7ad5a-112">Konto Data Lake Analytics, aby zaktualizować regułę zapory w</span><span class="sxs-lookup"><span data-stu-id="7ad5a-112">The Data Lake Analytics account to update the firewall rule in</span></span>

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

### <span data-ttu-id="7ad5a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ad5a-113">-DefaultProfile</span></span>
<span data-ttu-id="7ad5a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="7ad5a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7ad5a-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="7ad5a-115">-EndIpAddress</span></span>
<span data-ttu-id="7ad5a-116">Koniec prawidłowego zakresu adresów IP reguły zapory</span><span class="sxs-lookup"><span data-stu-id="7ad5a-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ad5a-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7ad5a-117">-Name</span></span>
<span data-ttu-id="7ad5a-118">Nazwa reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="7ad5a-118">The name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ad5a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ad5a-119">-ResourceGroupName</span></span>
<span data-ttu-id="7ad5a-120">Nazwa grupy zasobów, w ramach której chcesz pobrać konto.</span><span class="sxs-lookup"><span data-stu-id="7ad5a-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="7ad5a-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="7ad5a-121">-StartIpAddress</span></span>
<span data-ttu-id="7ad5a-122">Początek prawidłowego zakresu adresów IP reguły zapory</span><span class="sxs-lookup"><span data-stu-id="7ad5a-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="7ad5a-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7ad5a-123">-Confirm</span></span>
<span data-ttu-id="7ad5a-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7ad5a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ad5a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ad5a-125">-WhatIf</span></span>
<span data-ttu-id="7ad5a-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ad5a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ad5a-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7ad5a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ad5a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ad5a-128">CommonParameters</span></span>
<span data-ttu-id="7ad5a-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ad5a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ad5a-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ad5a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ad5a-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ad5a-131">INPUTS</span></span>

### <span data-ttu-id="7ad5a-132">System.String</span><span class="sxs-lookup"><span data-stu-id="7ad5a-132">System.String</span></span>

## <span data-ttu-id="7ad5a-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7ad5a-133">OUTPUTS</span></span>

### <span data-ttu-id="7ad5a-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7ad5a-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="7ad5a-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7ad5a-135">NOTES</span></span>

## <span data-ttu-id="7ad5a-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7ad5a-136">RELATED LINKS</span></span>
