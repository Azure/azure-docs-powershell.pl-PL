---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 6C7A7E1A-87A2-4F0D-9091-413C111F47F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: e583379f9541c056943081b804a84ecd7bee7bf5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238179"
---
# <span data-ttu-id="1d680-101">Remove-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1d680-101">Remove-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="1d680-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d680-102">SYNOPSIS</span></span>
<span data-ttu-id="1d680-103">Usuwa określoną regułę zapory w określonym magazynie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1d680-103">Removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="1d680-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1d680-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1d680-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="1d680-105">DESCRIPTION</span></span>
<span data-ttu-id="1d680-106">Polecenie **cmdlet Remove-AzDataLakeStoreFirewallRule** usuwa określoną regułę zapory w określonym magazynie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1d680-106">The **Remove-AzDataLakeStoreFirewallRule** cmdlet removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="1d680-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1d680-107">EXAMPLES</span></span>

### <span data-ttu-id="1d680-108">Przykład 1. Usuwanie reguły zapory z konta</span><span class="sxs-lookup"><span data-stu-id="1d680-108">Example 1: Remove a firewall rule from an account</span></span>
```
PS C:\> Remove-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="1d680-109">Usuwa regułę zapory "MyFirewallRule" z konta "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="1d680-109">Removes firewall rule "MyFirewallRule" from account "ContosoADL"</span></span>

## <span data-ttu-id="1d680-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d680-110">PARAMETERS</span></span>

### <span data-ttu-id="1d680-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="1d680-111">-Account</span></span>
<span data-ttu-id="1d680-112">Konto usługi Data Lake Store w celu zaktualizowania reguły zapory w</span><span class="sxs-lookup"><span data-stu-id="1d680-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="1d680-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d680-113">-DefaultProfile</span></span>
<span data-ttu-id="1d680-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="1d680-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1d680-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1d680-115">-Name</span></span>
<span data-ttu-id="1d680-116">Nazwa reguły zapory do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="1d680-116">The name of the firewall rule to delete.</span></span>

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

### <span data-ttu-id="1d680-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1d680-117">-PassThru</span></span>
<span data-ttu-id="1d680-118">Wskazuje, że powinna zostać zwrócona odpowiedź logiczna wskazująca wynik operacji usuwania.</span><span class="sxs-lookup"><span data-stu-id="1d680-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="1d680-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d680-119">-ResourceGroupName</span></span>
<span data-ttu-id="1d680-120">Określa nazwę grupy zasobów zawierającej konto, z których ma być usuwana reguła zapory.</span><span class="sxs-lookup"><span data-stu-id="1d680-120">Specifies the name of the resource group that contains the account to remove the firewall rule from.</span></span>

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

### <span data-ttu-id="1d680-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1d680-121">-Confirm</span></span>
<span data-ttu-id="1d680-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1d680-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d680-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d680-123">-WhatIf</span></span>
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

### <span data-ttu-id="1d680-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d680-124">CommonParameters</span></span>
<span data-ttu-id="1d680-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d680-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d680-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d680-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d680-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1d680-127">INPUTS</span></span>

### <span data-ttu-id="1d680-128">System.String</span><span class="sxs-lookup"><span data-stu-id="1d680-128">System.String</span></span>

### <span data-ttu-id="1d680-129">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="1d680-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1d680-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1d680-130">OUTPUTS</span></span>

### <span data-ttu-id="1d680-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1d680-131">System.Boolean</span></span>

## <span data-ttu-id="1d680-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1d680-132">NOTES</span></span>

## <span data-ttu-id="1d680-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1d680-133">RELATED LINKS</span></span>
