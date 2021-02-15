---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
ms.openlocfilehash: 562a2fbf02bd6389b28543f09ace1c59b2e9ed1c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202595"
---
# <span data-ttu-id="283c2-101">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="283c2-101">Remove-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="283c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="283c2-102">SYNOPSIS</span></span>
<span data-ttu-id="283c2-103">Usuwa grupę zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="283c2-103">Removes an application security group.</span></span>

## <span data-ttu-id="283c2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="283c2-104">SYNTAX</span></span>

```
Remove-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="283c2-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="283c2-105">DESCRIPTION</span></span>
<span data-ttu-id="283c2-106">Polecenie **cmdlet Remove-AzApplicationSecurityGroup** usuwa grupę zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="283c2-106">The **Remove-AzApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="283c2-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="283c2-107">EXAMPLES</span></span>

### <span data-ttu-id="283c2-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="283c2-108">Example 1</span></span>
```
PS C:\>Remove-AzApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="283c2-109">To polecenie usuwa grupę zabezpieczeń aplikacji o nazwie MyApplicationSecurityGrouo z grupy zasobów o nazwie MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="283c2-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="283c2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="283c2-110">PARAMETERS</span></span>

### <span data-ttu-id="283c2-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="283c2-111">-AsJob</span></span>
<span data-ttu-id="283c2-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="283c2-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="283c2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="283c2-113">-DefaultProfile</span></span>
<span data-ttu-id="283c2-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="283c2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="283c2-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="283c2-115">-Force</span></span>
<span data-ttu-id="283c2-116">Nie pytaj o potwierdzenie, czy chcesz usunąć zasób</span><span class="sxs-lookup"><span data-stu-id="283c2-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="283c2-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="283c2-117">-Name</span></span>
<span data-ttu-id="283c2-118">Nazwa grupy zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="283c2-118">The name of the application security group.</span></span>

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

### <span data-ttu-id="283c2-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="283c2-119">-PassThru</span></span>
<span data-ttu-id="283c2-120">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="283c2-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="283c2-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="283c2-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="283c2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="283c2-122">-ResourceGroupName</span></span>
<span data-ttu-id="283c2-123">Nazwa grupy zasobów grupy zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="283c2-123">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="283c2-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="283c2-124">-Confirm</span></span>
<span data-ttu-id="283c2-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="283c2-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="283c2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="283c2-126">-WhatIf</span></span>
<span data-ttu-id="283c2-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="283c2-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="283c2-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="283c2-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="283c2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="283c2-129">CommonParameters</span></span>
<span data-ttu-id="283c2-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="283c2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="283c2-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="283c2-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="283c2-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="283c2-132">INPUTS</span></span>

### <span data-ttu-id="283c2-133">System.String</span><span class="sxs-lookup"><span data-stu-id="283c2-133">System.String</span></span>

## <span data-ttu-id="283c2-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="283c2-134">OUTPUTS</span></span>

### <span data-ttu-id="283c2-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="283c2-135">System.Boolean</span></span>

## <span data-ttu-id="283c2-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="283c2-136">NOTES</span></span>

## <span data-ttu-id="283c2-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="283c2-137">RELATED LINKS</span></span>

[<span data-ttu-id="283c2-138">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="283c2-138">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="283c2-139">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="283c2-139">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)
