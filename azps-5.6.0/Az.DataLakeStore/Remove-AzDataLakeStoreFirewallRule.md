---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 6C7A7E1A-87A2-4F0D-9091-413C111F47F0
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/remove-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: 7a753f721e008a0c40f6a690d5c595a524ddc12b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964762"
---
# <span data-ttu-id="7a879-101">Remove-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7a879-101">Remove-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="7a879-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a879-102">SYNOPSIS</span></span>
<span data-ttu-id="7a879-103">Usuwa określoną regułę zapory w określonym magazynie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7a879-103">Removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="7a879-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7a879-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7a879-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="7a879-105">DESCRIPTION</span></span>
<span data-ttu-id="7a879-106">Polecenie **cmdlet Remove-AzDataLakeStoreFirewallRule** usuwa określoną regułę zapory w określonym magazynie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7a879-106">The **Remove-AzDataLakeStoreFirewallRule** cmdlet removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="7a879-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7a879-107">EXAMPLES</span></span>

### <span data-ttu-id="7a879-108">Przykład 1. Usuwanie reguły zapory z konta</span><span class="sxs-lookup"><span data-stu-id="7a879-108">Example 1: Remove a firewall rule from an account</span></span>
```
PS C:\> Remove-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="7a879-109">Usuwa regułę zapory "MyFirewallRule" z konta "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="7a879-109">Removes firewall rule "MyFirewallRule" from account "ContosoADL"</span></span>

## <span data-ttu-id="7a879-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a879-110">PARAMETERS</span></span>

### <span data-ttu-id="7a879-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="7a879-111">-Account</span></span>
<span data-ttu-id="7a879-112">Konto usługi Data Lake Store w celu zaktualizowania reguły zapory w</span><span class="sxs-lookup"><span data-stu-id="7a879-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="7a879-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a879-113">-DefaultProfile</span></span>
<span data-ttu-id="7a879-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="7a879-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a879-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7a879-115">-Name</span></span>
<span data-ttu-id="7a879-116">Nazwa reguły zapory do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="7a879-116">The name of the firewall rule to delete.</span></span>

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

### <span data-ttu-id="7a879-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a879-117">-PassThru</span></span>
<span data-ttu-id="7a879-118">Wskazuje, że powinna zostać zwrócona odpowiedź logiczna wskazująca wynik operacji usuwania.</span><span class="sxs-lookup"><span data-stu-id="7a879-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="7a879-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a879-119">-ResourceGroupName</span></span>
<span data-ttu-id="7a879-120">Określa nazwę grupy zasobów zawierającej konto, z których ma być usuwana reguła zapory.</span><span class="sxs-lookup"><span data-stu-id="7a879-120">Specifies the name of the resource group that contains the account to remove the firewall rule from.</span></span>

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

### <span data-ttu-id="7a879-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7a879-121">-Confirm</span></span>
<span data-ttu-id="7a879-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7a879-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a879-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a879-123">-WhatIf</span></span>
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

### <span data-ttu-id="7a879-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a879-124">CommonParameters</span></span>
<span data-ttu-id="7a879-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a879-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a879-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a879-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a879-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a879-127">INPUTS</span></span>

### <span data-ttu-id="7a879-128">System.String</span><span class="sxs-lookup"><span data-stu-id="7a879-128">System.String</span></span>

### <span data-ttu-id="7a879-129">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="7a879-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7a879-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a879-130">OUTPUTS</span></span>

### <span data-ttu-id="7a879-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7a879-131">System.Boolean</span></span>

## <span data-ttu-id="7a879-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7a879-132">NOTES</span></span>

## <span data-ttu-id="7a879-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7a879-133">RELATED LINKS</span></span>
