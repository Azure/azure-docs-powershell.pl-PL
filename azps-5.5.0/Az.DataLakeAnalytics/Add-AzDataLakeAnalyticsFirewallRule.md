---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/add-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: d9e6dd2e3fedff0d97919e04ca4f8b61536e2075
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242746"
---
# <span data-ttu-id="ec867-101">Add-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ec867-101">Add-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="ec867-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec867-102">SYNOPSIS</span></span>
<span data-ttu-id="ec867-103">Dodaje regułę zapory do konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="ec867-103">Adds a firewall rule to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="ec867-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ec867-104">SYNTAX</span></span>

```
Add-AzDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec867-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ec867-105">DESCRIPTION</span></span>
<span data-ttu-id="ec867-106">Polecenie **cmdlet Add-AzDataLakeAnalyticsFirewallRule** dodaje regułę zapory do konta usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="ec867-106">The **Add-AzDataLakeAnalyticsFirewallRule** cmdlet adds a firewall rule to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="ec867-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ec867-107">EXAMPLES</span></span>

### <span data-ttu-id="ec867-108">Przykład 1. Dodawanie reguły zapory</span><span class="sxs-lookup"><span data-stu-id="ec867-108">Example 1: Add a firewall rule</span></span>
```
PS C:\>Add-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="ec867-109">To polecenie dodaje regułę zapory o nazwie "reguła zapory" z konta "ContosoAdlAcct" z zakresem adresów IP: 127.0.0.1 – 127.0.0.10</span><span class="sxs-lookup"><span data-stu-id="ec867-109">This command adds the firewall rule named "my firewall rule" from account "ContosoAdlAcct" with the IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="ec867-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec867-110">PARAMETERS</span></span>

### <span data-ttu-id="ec867-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="ec867-111">-Account</span></span>
<span data-ttu-id="ec867-112">Konto Data Lake Analytics, aby dodać regułę zapory do</span><span class="sxs-lookup"><span data-stu-id="ec867-112">The Data Lake Analytics account to add the firewall rule to</span></span>

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

### <span data-ttu-id="ec867-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec867-113">-DefaultProfile</span></span>
<span data-ttu-id="ec867-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="ec867-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ec867-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="ec867-115">-EndIpAddress</span></span>
<span data-ttu-id="ec867-116">Koniec prawidłowego zakresu adresów IP reguły zapory</span><span class="sxs-lookup"><span data-stu-id="ec867-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec867-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ec867-117">-Name</span></span>
<span data-ttu-id="ec867-118">Nazwa reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="ec867-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="ec867-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec867-119">-ResourceGroupName</span></span>
<span data-ttu-id="ec867-120">Nazwa grupy zasobów, w ramach której chcesz pobrać konto.</span><span class="sxs-lookup"><span data-stu-id="ec867-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="ec867-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="ec867-121">-StartIpAddress</span></span>
<span data-ttu-id="ec867-122">Początek prawidłowego zakresu adresów IP reguły zapory</span><span class="sxs-lookup"><span data-stu-id="ec867-122">The start of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec867-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ec867-123">-Confirm</span></span>
<span data-ttu-id="ec867-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ec867-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec867-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec867-125">-WhatIf</span></span>
<span data-ttu-id="ec867-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec867-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec867-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ec867-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec867-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec867-128">CommonParameters</span></span>
<span data-ttu-id="ec867-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec867-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec867-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec867-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec867-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ec867-131">INPUTS</span></span>

### <span data-ttu-id="ec867-132">System.String</span><span class="sxs-lookup"><span data-stu-id="ec867-132">System.String</span></span>

## <span data-ttu-id="ec867-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ec867-133">OUTPUTS</span></span>

### <span data-ttu-id="ec867-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ec867-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="ec867-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ec867-135">NOTES</span></span>

## <span data-ttu-id="ec867-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ec867-136">RELATED LINKS</span></span>
