---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: C6FD4734-720C-4C8C-9B58-EDB331DD6415
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: 9fa890ee6102f4751b62325b3cc3669d337cb6c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868571"
---
# <span data-ttu-id="95dc4-101">Add-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="95dc4-101">Add-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="95dc4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="95dc4-102">SYNOPSIS</span></span>
<span data-ttu-id="95dc4-103">Umożliwia dodanie reguły zapory do określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="95dc4-103">Adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="95dc4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="95dc4-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95dc4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="95dc4-105">DESCRIPTION</span></span>
<span data-ttu-id="95dc4-106">Polecenie cmdlet **Add-AzDataLakeStoreFirewallRule** umożliwia dodanie reguły zapory do określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="95dc4-106">The **Add-AzDataLakeStoreFirewallRule** cmdlet adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="95dc4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="95dc4-107">EXAMPLES</span></span>

### <span data-ttu-id="95dc4-108">Przykład 1: Dodawanie nowej reguły zapory do konta usługi Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="95dc4-108">Example 1: Add a new firewall rule to a Data Lake Store account</span></span>
```
PS C:\> Add-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="95dc4-109">Spowoduje to utworzenie nowej reguły zapory o nazwie "Moja reguła" na koncie "ContosoADL" z zakresem adresów IP 127.0.0.1-127.0.0.2</span><span class="sxs-lookup"><span data-stu-id="95dc4-109">This creates a new firewall rule called "MyRule" in account "ContosoADL" with an IP range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="95dc4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="95dc4-110">PARAMETERS</span></span>

### <span data-ttu-id="95dc4-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="95dc4-111">-Account</span></span>
<span data-ttu-id="95dc4-112">Konto usługi Data Lake Store, do którego ma zostać dodana reguła zapory</span><span class="sxs-lookup"><span data-stu-id="95dc4-112">The Data Lake Store account to add the firewall rule to</span></span>

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

### <span data-ttu-id="95dc4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95dc4-113">-DefaultProfile</span></span>
<span data-ttu-id="95dc4-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="95dc4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="95dc4-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="95dc4-115">-EndIpAddress</span></span>
<span data-ttu-id="95dc4-116">Koniec prawidłowego zakresu adresów IP dla reguły zapory</span><span class="sxs-lookup"><span data-stu-id="95dc4-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="95dc4-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="95dc4-117">-Name</span></span>
<span data-ttu-id="95dc4-118">Nazwa reguły zapory, którą należy dodać.</span><span class="sxs-lookup"><span data-stu-id="95dc4-118">The name of the firewall rule to add.</span></span>

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

### <span data-ttu-id="95dc4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95dc4-119">-ResourceGroupName</span></span>
<span data-ttu-id="95dc4-120">Nazwa grupy zasobów, pod którą konto do dodania reguły zapory jest.</span><span class="sxs-lookup"><span data-stu-id="95dc4-120">Name of resource group under which the account to add the firewall rule is.</span></span>

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

### <span data-ttu-id="95dc4-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="95dc4-121">-StartIpAddress</span></span>
<span data-ttu-id="95dc4-122">Początek prawidłowego zakresu adresów IP dla reguły zapory</span><span class="sxs-lookup"><span data-stu-id="95dc4-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="95dc4-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="95dc4-123">-Confirm</span></span>
<span data-ttu-id="95dc4-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95dc4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95dc4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95dc4-125">-WhatIf</span></span>
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

### <span data-ttu-id="95dc4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95dc4-126">CommonParameters</span></span>
<span data-ttu-id="95dc4-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95dc4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95dc4-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95dc4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95dc4-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="95dc4-129">INPUTS</span></span>

### <span data-ttu-id="95dc4-130">System. String</span><span class="sxs-lookup"><span data-stu-id="95dc4-130">System.String</span></span>

## <span data-ttu-id="95dc4-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="95dc4-131">OUTPUTS</span></span>

### <span data-ttu-id="95dc4-132">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="95dc4-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="95dc4-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="95dc4-133">NOTES</span></span>

## <span data-ttu-id="95dc4-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="95dc4-134">RELATED LINKS</span></span>
