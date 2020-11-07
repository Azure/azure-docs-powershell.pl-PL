---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 8d69a3297f23fdc9e4095a695ee790ae2476a136
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868595"
---
# <span data-ttu-id="5d977-101">Set-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5d977-101">Set-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="5d977-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5d977-102">SYNOPSIS</span></span>
<span data-ttu-id="5d977-103">Umożliwia zaktualizowanie reguły zapory na koncie danych w usłudze Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="5d977-103">Updates a firewall rule in a Data Lake Analytics account.</span></span>

## <span data-ttu-id="5d977-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5d977-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d977-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5d977-105">DESCRIPTION</span></span>
<span data-ttu-id="5d977-106">Polecenie cmdlet **Set-AzDataLakeAnalyticsFirewallRule** umożliwia zaktualizowanie reguły zapory na koncie usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="5d977-106">The **Set-AzDataLakeAnalyticsFirewallRule** cmdlet updates a firewall rule in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="5d977-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5d977-107">EXAMPLES</span></span>

### <span data-ttu-id="5d977-108">Przykład 1: aktualizowanie reguły zapory</span><span class="sxs-lookup"><span data-stu-id="5d977-108">Example 1: Update a firewall rule</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="5d977-109">To polecenie powoduje zaktualizowanie reguły zapory o nazwie "Moja Reguła zapory" na koncie "ContosoAdlAcct" w celu uzyskania nowego zakresu adresów IP: 127.0.0.1-127.0.0.10</span><span class="sxs-lookup"><span data-stu-id="5d977-109">This command updates the firewall rule named "my firewall rule" in account "ContosoAdlAcct" to have the new IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="5d977-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5d977-110">PARAMETERS</span></span>

### <span data-ttu-id="5d977-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="5d977-111">-Account</span></span>
<span data-ttu-id="5d977-112">Konto usługi Data Lake Analytics do aktualizowania reguły zapory w</span><span class="sxs-lookup"><span data-stu-id="5d977-112">The Data Lake Analytics account to update the firewall rule in</span></span>

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

### <span data-ttu-id="5d977-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d977-113">-DefaultProfile</span></span>
<span data-ttu-id="5d977-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5d977-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d977-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="5d977-115">-EndIpAddress</span></span>
<span data-ttu-id="5d977-116">Koniec prawidłowego zakresu adresów IP dla reguły zapory</span><span class="sxs-lookup"><span data-stu-id="5d977-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="5d977-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5d977-117">-Name</span></span>
<span data-ttu-id="5d977-118">Nazwa reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="5d977-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="5d977-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d977-119">-ResourceGroupName</span></span>
<span data-ttu-id="5d977-120">Nazwa grupy zasobów, pod którą ma zostać pobrane konto.</span><span class="sxs-lookup"><span data-stu-id="5d977-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="5d977-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="5d977-121">-StartIpAddress</span></span>
<span data-ttu-id="5d977-122">Początek prawidłowego zakresu adresów IP dla reguły zapory</span><span class="sxs-lookup"><span data-stu-id="5d977-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="5d977-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5d977-123">-Confirm</span></span>
<span data-ttu-id="5d977-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d977-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d977-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d977-125">-WhatIf</span></span>
<span data-ttu-id="5d977-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d977-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d977-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5d977-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d977-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d977-128">CommonParameters</span></span>
<span data-ttu-id="5d977-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d977-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d977-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d977-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d977-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5d977-131">INPUTS</span></span>

### <span data-ttu-id="5d977-132">System. String</span><span class="sxs-lookup"><span data-stu-id="5d977-132">System.String</span></span>

## <span data-ttu-id="5d977-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5d977-133">OUTPUTS</span></span>

### <span data-ttu-id="5d977-134">Microsoft. Azure. Commands. DataLakeAnalytics. models. DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5d977-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="5d977-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5d977-135">NOTES</span></span>

## <span data-ttu-id="5d977-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5d977-136">RELATED LINKS</span></span>
