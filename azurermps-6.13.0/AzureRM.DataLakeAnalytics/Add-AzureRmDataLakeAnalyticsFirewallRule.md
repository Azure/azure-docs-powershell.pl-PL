---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/add-azurermdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 93f951632ade49949780b970e4910c98887fe863
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716781"
---
# <span data-ttu-id="702b1-101">Add-AzureRmDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="702b1-101">Add-AzureRmDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="702b1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="702b1-102">SYNOPSIS</span></span>
<span data-ttu-id="702b1-103">Dodaje regułę zapory do konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="702b1-103">Adds a firewall rule to a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="702b1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="702b1-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="702b1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="702b1-105">DESCRIPTION</span></span>
<span data-ttu-id="702b1-106">Polecenie cmdlet **Add-AzureRmDataLakeAnalyticsFirewallRule** umożliwia dodanie reguły zapory do konta usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="702b1-106">The **Add-AzureRmDataLakeAnalyticsFirewallRule** cmdlet adds a firewall rule to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="702b1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="702b1-107">EXAMPLES</span></span>

### <span data-ttu-id="702b1-108">Przykład 1: Dodawanie reguły zapory</span><span class="sxs-lookup"><span data-stu-id="702b1-108">Example 1: Add a firewall rule</span></span>
```
PS C:\>Add-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="702b1-109">To polecenie dodaje regułę zapory o nazwie "Moja Reguła zapory" z konta "ContosoAdlAcct" z zakresem adresów IP: 127.0.0.1-127.0.0.10</span><span class="sxs-lookup"><span data-stu-id="702b1-109">This command adds the firewall rule named "my firewall rule" from account "ContosoAdlAcct" with the IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="702b1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="702b1-110">PARAMETERS</span></span>

### <span data-ttu-id="702b1-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="702b1-111">-Account</span></span>
<span data-ttu-id="702b1-112">Konto usługi Data Lake Analytics, do którego ma zostać dodana reguła zapory</span><span class="sxs-lookup"><span data-stu-id="702b1-112">The Data Lake Analytics account to add the firewall rule to</span></span>

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

### <span data-ttu-id="702b1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="702b1-113">-DefaultProfile</span></span>
<span data-ttu-id="702b1-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="702b1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="702b1-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="702b1-115">-EndIpAddress</span></span>
<span data-ttu-id="702b1-116">Koniec prawidłowego zakresu adresów IP dla reguły zapory</span><span class="sxs-lookup"><span data-stu-id="702b1-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="702b1-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="702b1-117">-Name</span></span>
<span data-ttu-id="702b1-118">Nazwa reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="702b1-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="702b1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="702b1-119">-ResourceGroupName</span></span>
<span data-ttu-id="702b1-120">Nazwa grupy zasobów, pod którą ma zostać pobrane konto.</span><span class="sxs-lookup"><span data-stu-id="702b1-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="702b1-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="702b1-121">-StartIpAddress</span></span>
<span data-ttu-id="702b1-122">Początek prawidłowego zakresu adresów IP dla reguły zapory</span><span class="sxs-lookup"><span data-stu-id="702b1-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="702b1-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="702b1-123">-Confirm</span></span>
<span data-ttu-id="702b1-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="702b1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="702b1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="702b1-125">-WhatIf</span></span>
<span data-ttu-id="702b1-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="702b1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="702b1-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="702b1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="702b1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="702b1-128">CommonParameters</span></span>
<span data-ttu-id="702b1-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="702b1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="702b1-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="702b1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="702b1-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="702b1-131">INPUTS</span></span>

### <span data-ttu-id="702b1-132">System. String</span><span class="sxs-lookup"><span data-stu-id="702b1-132">System.String</span></span>

## <span data-ttu-id="702b1-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="702b1-133">OUTPUTS</span></span>

### <span data-ttu-id="702b1-134">Microsoft. Azure. Commands. DataLakeAnalytics. models. DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="702b1-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="702b1-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="702b1-135">NOTES</span></span>

## <span data-ttu-id="702b1-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="702b1-136">RELATED LINKS</span></span>
