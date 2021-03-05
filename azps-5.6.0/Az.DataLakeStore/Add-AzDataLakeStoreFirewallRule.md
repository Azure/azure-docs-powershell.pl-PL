---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: C6FD4734-720C-4C8C-9B58-EDB331DD6415
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/add-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: 60a3363716bb4e93efa02cc63d3e83548c4944f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004250"
---
# <span data-ttu-id="4d628-101">Add-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4d628-101">Add-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="4d628-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d628-102">SYNOPSIS</span></span>
<span data-ttu-id="4d628-103">Dodaje regułę zapory do określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4d628-103">Adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="4d628-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4d628-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d628-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4d628-105">DESCRIPTION</span></span>
<span data-ttu-id="4d628-106">Polecenie **cmdlet Add-AzDataLakeStoreFirewallRule** dodaje regułę zapory do określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4d628-106">The **Add-AzDataLakeStoreFirewallRule** cmdlet adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="4d628-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4d628-107">EXAMPLES</span></span>

### <span data-ttu-id="4d628-108">Przykład 1. Dodawanie nowej reguły zapory do konta usługi Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="4d628-108">Example 1: Add a new firewall rule to a Data Lake Store account</span></span>
```
PS C:\> Add-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="4d628-109">Powoduje to utworzenie nowej reguły zapory o nazwie "MyRule" na koncie "ContosoADL" z zakresem adresów IP od 127.0.0.1 do 127.0.0.2</span><span class="sxs-lookup"><span data-stu-id="4d628-109">This creates a new firewall rule called "MyRule" in account "ContosoADL" with an IP range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="4d628-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d628-110">PARAMETERS</span></span>

### <span data-ttu-id="4d628-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="4d628-111">-Account</span></span>
<span data-ttu-id="4d628-112">Konto usługi Data Lake Store w celu dodania reguły zapory do</span><span class="sxs-lookup"><span data-stu-id="4d628-112">The Data Lake Store account to add the firewall rule to</span></span>

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

### <span data-ttu-id="4d628-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d628-113">-DefaultProfile</span></span>
<span data-ttu-id="4d628-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="4d628-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d628-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="4d628-115">-EndIpAddress</span></span>
<span data-ttu-id="4d628-116">Koniec prawidłowego zakresu adresów IP reguły zapory</span><span class="sxs-lookup"><span data-stu-id="4d628-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="4d628-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4d628-117">-Name</span></span>
<span data-ttu-id="4d628-118">Nazwa reguły zapory, która ma być dodawania.</span><span class="sxs-lookup"><span data-stu-id="4d628-118">The name of the firewall rule to add.</span></span>

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

### <span data-ttu-id="4d628-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d628-119">-ResourceGroupName</span></span>
<span data-ttu-id="4d628-120">Nazwa grupy zasobów, w której znajduje się konto, do którego należy dodać regułę zapory.</span><span class="sxs-lookup"><span data-stu-id="4d628-120">Name of resource group under which the account to add the firewall rule is.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d628-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="4d628-121">-StartIpAddress</span></span>
<span data-ttu-id="4d628-122">Początek prawidłowego zakresu adresów IP reguły zapory</span><span class="sxs-lookup"><span data-stu-id="4d628-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="4d628-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4d628-123">-Confirm</span></span>
<span data-ttu-id="4d628-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4d628-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d628-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d628-125">-WhatIf</span></span>
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

### <span data-ttu-id="4d628-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d628-126">CommonParameters</span></span>
<span data-ttu-id="4d628-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d628-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d628-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d628-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d628-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d628-129">INPUTS</span></span>

### <span data-ttu-id="4d628-130">System.String</span><span class="sxs-lookup"><span data-stu-id="4d628-130">System.String</span></span>

## <span data-ttu-id="4d628-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d628-131">OUTPUTS</span></span>

### <span data-ttu-id="4d628-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4d628-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="4d628-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4d628-133">NOTES</span></span>

## <span data-ttu-id="4d628-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4d628-134">RELATED LINKS</span></span>
