---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 6C7A7E1A-87A2-4F0D-9091-413C111F47F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 7e762ed090b0076c5cc8d0b359cf8883ae26265d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524458"
---
# <span data-ttu-id="41227-101">Remove-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="41227-101">Remove-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="41227-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="41227-102">SYNOPSIS</span></span>
<span data-ttu-id="41227-103">Usuwa określoną regułę zapory w określonym sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="41227-103">Removes the specified firewall rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41227-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="41227-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="41227-105">Opis</span><span class="sxs-lookup"><span data-stu-id="41227-105">DESCRIPTION</span></span>
<span data-ttu-id="41227-106">Polecenie cmdlet **Remove-AzureRmDataLakeStoreFirewallRule** usuwa określoną regułę zapory w określonym sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="41227-106">The **Remove-AzureRmDataLakeStoreFirewallRule** cmdlet removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="41227-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="41227-107">EXAMPLES</span></span>

### <span data-ttu-id="41227-108">Przykład 1: Usuwanie reguły zapory z konta</span><span class="sxs-lookup"><span data-stu-id="41227-108">Example 1: Remove a firewall rule from an account</span></span>
```
PS C:\> Remove-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="41227-109">Usuwa regułę zapory "MyFirewallRule" z konta "ContosoADL".</span><span class="sxs-lookup"><span data-stu-id="41227-109">Removes firewall rule "MyFirewallRule" from account "ContosoADL"</span></span>

## <span data-ttu-id="41227-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="41227-110">PARAMETERS</span></span>

### <span data-ttu-id="41227-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="41227-111">-Account</span></span>
<span data-ttu-id="41227-112">Konto usługi Data Lake Store do aktualizowania reguły zapory</span><span class="sxs-lookup"><span data-stu-id="41227-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="41227-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41227-113">-DefaultProfile</span></span>
<span data-ttu-id="41227-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="41227-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="41227-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="41227-115">-Name</span></span>
<span data-ttu-id="41227-116">Nazwa reguły zapory do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="41227-116">The name of the firewall rule to delete.</span></span>

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

### <span data-ttu-id="41227-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41227-117">-PassThru</span></span>
<span data-ttu-id="41227-118">Wskazuje, że należy zwrócić odpowiedź logiczną wskazującą wynik operacji usuwania.</span><span class="sxs-lookup"><span data-stu-id="41227-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="41227-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41227-119">-ResourceGroupName</span></span>
<span data-ttu-id="41227-120">Określa nazwę grupy zasobów zawierającej konto, z którego ma zostać usunięta Reguła zapory.</span><span class="sxs-lookup"><span data-stu-id="41227-120">Specifies the name of the resource group that contains the account to remove the firewall rule from.</span></span>

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

### <span data-ttu-id="41227-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="41227-121">-Confirm</span></span>
<span data-ttu-id="41227-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41227-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41227-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41227-123">-WhatIf</span></span>
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

### <span data-ttu-id="41227-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41227-124">CommonParameters</span></span>
<span data-ttu-id="41227-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41227-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41227-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41227-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41227-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41227-127">INPUTS</span></span>

### <span data-ttu-id="41227-128">System. String</span><span class="sxs-lookup"><span data-stu-id="41227-128">System.String</span></span>

### <span data-ttu-id="41227-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="41227-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="41227-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="41227-130">OUTPUTS</span></span>

### <span data-ttu-id="41227-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="41227-131">System.Boolean</span></span>

## <span data-ttu-id="41227-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="41227-132">NOTES</span></span>

## <span data-ttu-id="41227-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="41227-133">RELATED LINKS</span></span>
