---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 6f19df2f234bd66ac629f8238aa2cfea257106df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718230"
---
# <span data-ttu-id="bdd90-101">Set-AzureRmDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bdd90-101">Set-AzureRmDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="bdd90-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bdd90-102">SYNOPSIS</span></span>
<span data-ttu-id="bdd90-103">Umożliwia zaktualizowanie reguły zapory na koncie danych w usłudze Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="bdd90-103">Updates a firewall rule in a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bdd90-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bdd90-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdd90-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bdd90-105">DESCRIPTION</span></span>
<span data-ttu-id="bdd90-106">Polecenie cmdlet **Set-AzureRmDataLakeAnalyticsFirewallRule** umożliwia zaktualizowanie reguły zapory na koncie usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="bdd90-106">The **Set-AzureRmDataLakeAnalyticsFirewallRule** cmdlet updates a firewall rule in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="bdd90-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bdd90-107">EXAMPLES</span></span>

### <span data-ttu-id="bdd90-108">Przykład 1: aktualizowanie reguły zapory</span><span class="sxs-lookup"><span data-stu-id="bdd90-108">Example 1: Update a firewall rule</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="bdd90-109">To polecenie powoduje zaktualizowanie reguły zapory o nazwie "Moja Reguła zapory" na koncie "ContosoAdlAcct" w celu uzyskania nowego zakresu adresów IP: 127.0.0.1-127.0.0.10</span><span class="sxs-lookup"><span data-stu-id="bdd90-109">This command updates the firewall rule named "my firewall rule" in account "ContosoAdlAcct" to have the new IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="bdd90-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bdd90-110">PARAMETERS</span></span>

### <span data-ttu-id="bdd90-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="bdd90-111">-Account</span></span>
<span data-ttu-id="bdd90-112">Konto usługi Data Lake Analytics do aktualizowania reguły zapory w</span><span class="sxs-lookup"><span data-stu-id="bdd90-112">The Data Lake Analytics account to update the firewall rule in</span></span>

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

### <span data-ttu-id="bdd90-113">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="bdd90-113">-EndIpAddress</span></span>
<span data-ttu-id="bdd90-114">Koniec prawidłowego zakresu adresów IP dla reguły zapory</span><span class="sxs-lookup"><span data-stu-id="bdd90-114">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="bdd90-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bdd90-115">-Name</span></span>
<span data-ttu-id="bdd90-116">Nazwa reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="bdd90-116">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="bdd90-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdd90-117">-ResourceGroupName</span></span>
<span data-ttu-id="bdd90-118">Nazwa grupy zasobów, pod którą ma zostać pobrane konto.</span><span class="sxs-lookup"><span data-stu-id="bdd90-118">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="bdd90-119">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="bdd90-119">-StartIpAddress</span></span>
<span data-ttu-id="bdd90-120">Początek prawidłowego zakresu adresów IP dla reguły zapory</span><span class="sxs-lookup"><span data-stu-id="bdd90-120">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="bdd90-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bdd90-121">-Confirm</span></span>
<span data-ttu-id="bdd90-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdd90-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdd90-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdd90-123">-WhatIf</span></span>
<span data-ttu-id="bdd90-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdd90-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdd90-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bdd90-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdd90-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdd90-126">-DefaultProfile</span></span>
<span data-ttu-id="bdd90-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bdd90-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdd90-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdd90-128">CommonParameters</span></span>
<span data-ttu-id="bdd90-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdd90-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdd90-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdd90-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdd90-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bdd90-131">INPUTS</span></span>

### <span data-ttu-id="bdd90-132">System. String</span><span class="sxs-lookup"><span data-stu-id="bdd90-132">System.String</span></span>

## <span data-ttu-id="bdd90-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bdd90-133">OUTPUTS</span></span>

### <span data-ttu-id="bdd90-134">Microsoft. Azure. Commands. DataLakeAnalytics. models. DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bdd90-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="bdd90-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bdd90-135">NOTES</span></span>

## <span data-ttu-id="bdd90-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bdd90-136">RELATED LINKS</span></span>

