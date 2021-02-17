---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9DBD5ADF-C30E-4D1A-A4CB-4D70C21088F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
ms.openlocfilehash: 52d2907769ac59a9c71fccef6baf08cc4d13bae8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184291"
---
# <span data-ttu-id="00d8c-101">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="00d8c-101">Remove-AzFirewall</span></span>

## <span data-ttu-id="00d8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00d8c-102">SYNOPSIS</span></span>
<span data-ttu-id="00d8c-103">Usuwanie Zapory.</span><span class="sxs-lookup"><span data-stu-id="00d8c-103">Remove a Firewall.</span></span>

## <span data-ttu-id="00d8c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="00d8c-104">SYNTAX</span></span>

```
Remove-AzFirewall -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00d8c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="00d8c-105">DESCRIPTION</span></span>
<span data-ttu-id="00d8c-106">Polecenie **cmdlet Remove-AzFirewall** usuwa Zaporę platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="00d8c-106">The **Remove-AzFirewall** cmdlet removes an Azure Firewall.</span></span>

## <span data-ttu-id="00d8c-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="00d8c-107">EXAMPLES</span></span>

### <span data-ttu-id="00d8c-108">Przykład 1. Tworzenie i usuwanie Zapory</span><span class="sxs-lookup"><span data-stu-id="00d8c-108">Example 1: Create and delete a Firewall</span></span>
```powershell
New-AzFirewall -Name "azFw" -ResourceGroupName "rgName" -Location centralus 

Remove-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="00d8c-109">W tym przykładzie zapora jest tworzą ją, a następnie usuwa.</span><span class="sxs-lookup"><span data-stu-id="00d8c-109">This example creates a Firewall and then deletes it.</span></span> <span data-ttu-id="00d8c-110">Aby pominąć monit podczas usuwania Zapory, użyj flagi -Force.</span><span class="sxs-lookup"><span data-stu-id="00d8c-110">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

## <span data-ttu-id="00d8c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00d8c-111">PARAMETERS</span></span>

### <span data-ttu-id="00d8c-112">— AsJob</span><span class="sxs-lookup"><span data-stu-id="00d8c-112">-AsJob</span></span>
<span data-ttu-id="00d8c-113">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="00d8c-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00d8c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00d8c-114">-DefaultProfile</span></span>
<span data-ttu-id="00d8c-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="00d8c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00d8c-116">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="00d8c-116">-Force</span></span>
<span data-ttu-id="00d8c-117">Wymusza uruchomienie polecenia bez pytania o potwierdzenie przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="00d8c-117">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00d8c-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="00d8c-118">-Name</span></span>
<span data-ttu-id="00d8c-119">Określa nazwę zapory, która jest usuwana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00d8c-119">Specifies the name of the firewall that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00d8c-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="00d8c-120">-PassThru</span></span>
<span data-ttu-id="00d8c-121">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="00d8c-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="00d8c-122">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="00d8c-122">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00d8c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00d8c-123">-ResourceGroupName</span></span>
<span data-ttu-id="00d8c-124">Określa nazwę grupy zasobów zawierającej zaporę usuwaną przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00d8c-124">Specifies the name of the resource group that contains the firewall that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00d8c-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="00d8c-125">-Confirm</span></span>
<span data-ttu-id="00d8c-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="00d8c-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00d8c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00d8c-127">-WhatIf</span></span>
<span data-ttu-id="00d8c-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00d8c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00d8c-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="00d8c-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00d8c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00d8c-130">CommonParameters</span></span>
<span data-ttu-id="00d8c-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00d8c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00d8c-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00d8c-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00d8c-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="00d8c-133">INPUTS</span></span>

### <span data-ttu-id="00d8c-134">System.String</span><span class="sxs-lookup"><span data-stu-id="00d8c-134">System.String</span></span>

## <span data-ttu-id="00d8c-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="00d8c-135">OUTPUTS</span></span>

### <span data-ttu-id="00d8c-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="00d8c-136">System.Boolean</span></span>

## <span data-ttu-id="00d8c-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="00d8c-137">NOTES</span></span>

## <span data-ttu-id="00d8c-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="00d8c-138">RELATED LINKS</span></span>

[<span data-ttu-id="00d8c-139">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="00d8c-139">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="00d8c-140">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="00d8c-140">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="00d8c-141">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="00d8c-141">Set-AzFirewall</span></span>](./Set-AzFirewall.md)
