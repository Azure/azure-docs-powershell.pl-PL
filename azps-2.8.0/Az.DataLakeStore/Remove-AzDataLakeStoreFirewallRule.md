---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 6C7A7E1A-87A2-4F0D-9091-413C111F47F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: e4764fff543666d677689a029f0fb5b3089a99bb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705790"
---
# <span data-ttu-id="f198c-101">Remove-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f198c-101">Remove-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="f198c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f198c-102">SYNOPSIS</span></span>
<span data-ttu-id="f198c-103">Usuwa określoną regułę zapory w określonym sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f198c-103">Removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="f198c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f198c-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f198c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f198c-105">DESCRIPTION</span></span>
<span data-ttu-id="f198c-106">Polecenie cmdlet **Remove-AzDataLakeStoreFirewallRule** usuwa określoną regułę zapory w określonym sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f198c-106">The **Remove-AzDataLakeStoreFirewallRule** cmdlet removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="f198c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f198c-107">EXAMPLES</span></span>

### <span data-ttu-id="f198c-108">Przykład 1: Usuwanie reguły zapory z konta</span><span class="sxs-lookup"><span data-stu-id="f198c-108">Example 1: Remove a firewall rule from an account</span></span>
```
PS C:\> Remove-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="f198c-109">Usuwa regułę zapory "MyFirewallRule" z konta "ContosoADL".</span><span class="sxs-lookup"><span data-stu-id="f198c-109">Removes firewall rule "MyFirewallRule" from account "ContosoADL"</span></span>

## <span data-ttu-id="f198c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f198c-110">PARAMETERS</span></span>

### <span data-ttu-id="f198c-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="f198c-111">-Account</span></span>
<span data-ttu-id="f198c-112">Konto usługi Data Lake Store do aktualizowania reguły zapory</span><span class="sxs-lookup"><span data-stu-id="f198c-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="f198c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f198c-113">-DefaultProfile</span></span>
<span data-ttu-id="f198c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f198c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f198c-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f198c-115">-Name</span></span>
<span data-ttu-id="f198c-116">Nazwa reguły zapory do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="f198c-116">The name of the firewall rule to delete.</span></span>

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

### <span data-ttu-id="f198c-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f198c-117">-PassThru</span></span>
<span data-ttu-id="f198c-118">Wskazuje, że należy zwrócić odpowiedź logiczną wskazującą wynik operacji usuwania.</span><span class="sxs-lookup"><span data-stu-id="f198c-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="f198c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f198c-119">-ResourceGroupName</span></span>
<span data-ttu-id="f198c-120">Określa nazwę grupy zasobów zawierającej konto, z którego ma zostać usunięta Reguła zapory.</span><span class="sxs-lookup"><span data-stu-id="f198c-120">Specifies the name of the resource group that contains the account to remove the firewall rule from.</span></span>

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

### <span data-ttu-id="f198c-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f198c-121">-Confirm</span></span>
<span data-ttu-id="f198c-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f198c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f198c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f198c-123">-WhatIf</span></span>
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

### <span data-ttu-id="f198c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f198c-124">CommonParameters</span></span>
<span data-ttu-id="f198c-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f198c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f198c-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f198c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f198c-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f198c-127">INPUTS</span></span>

### <span data-ttu-id="f198c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f198c-128">System.String</span></span>

### <span data-ttu-id="f198c-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f198c-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f198c-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f198c-130">OUTPUTS</span></span>

### <span data-ttu-id="f198c-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f198c-131">System.Boolean</span></span>

## <span data-ttu-id="f198c-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f198c-132">NOTES</span></span>

## <span data-ttu-id="f198c-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f198c-133">RELATED LINKS</span></span>