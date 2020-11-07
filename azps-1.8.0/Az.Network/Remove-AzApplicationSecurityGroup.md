---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
ms.openlocfilehash: 0af35c08cce181ba96f15ca77c0f17f96cfeb32e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709156"
---
# <span data-ttu-id="49710-101">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="49710-101">Remove-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="49710-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="49710-102">SYNOPSIS</span></span>
<span data-ttu-id="49710-103">Usuwa grupę zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="49710-103">Removes an application security group.</span></span>

## <span data-ttu-id="49710-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="49710-104">SYNTAX</span></span>

```
Remove-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49710-105">Opis</span><span class="sxs-lookup"><span data-stu-id="49710-105">DESCRIPTION</span></span>
<span data-ttu-id="49710-106">Polecenie cmdlet **Remove-AzApplicationSecurityGroup** usuwa grupę zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="49710-106">The **Remove-AzApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="49710-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="49710-107">EXAMPLES</span></span>

### <span data-ttu-id="49710-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="49710-108">Example 1</span></span>
```
PS C:\>Remove-AzApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="49710-109">To polecenie usuwa grupę zabezpieczeń aplikacji o nazwie MyApplicationSecurityGrouo w grupie zasobów o nazwie Moja zasobów.</span><span class="sxs-lookup"><span data-stu-id="49710-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="49710-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="49710-110">PARAMETERS</span></span>

### <span data-ttu-id="49710-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49710-111">-AsJob</span></span>
<span data-ttu-id="49710-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="49710-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="49710-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49710-113">-DefaultProfile</span></span>
<span data-ttu-id="49710-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="49710-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49710-115">-Force</span><span class="sxs-lookup"><span data-stu-id="49710-115">-Force</span></span>
<span data-ttu-id="49710-116">Nie pytaj o potwierdzenie, czy chcesz usunąć zasób</span><span class="sxs-lookup"><span data-stu-id="49710-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="49710-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="49710-117">-Name</span></span>
<span data-ttu-id="49710-118">Nazwa grupy zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="49710-118">The name of the application security group.</span></span>

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

### <span data-ttu-id="49710-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49710-119">-PassThru</span></span>
<span data-ttu-id="49710-120">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="49710-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="49710-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="49710-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="49710-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49710-122">-ResourceGroupName</span></span>
<span data-ttu-id="49710-123">Nazwa grupy zasobów grupy zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="49710-123">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="49710-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="49710-124">-Confirm</span></span>
<span data-ttu-id="49710-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49710-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49710-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49710-126">-WhatIf</span></span>
<span data-ttu-id="49710-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49710-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49710-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="49710-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49710-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49710-129">CommonParameters</span></span>
<span data-ttu-id="49710-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49710-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49710-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49710-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49710-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49710-132">INPUTS</span></span>

### <span data-ttu-id="49710-133">System. String</span><span class="sxs-lookup"><span data-stu-id="49710-133">System.String</span></span>

## <span data-ttu-id="49710-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="49710-134">OUTPUTS</span></span>

### <span data-ttu-id="49710-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="49710-135">System.Boolean</span></span>

## <span data-ttu-id="49710-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="49710-136">NOTES</span></span>

## <span data-ttu-id="49710-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="49710-137">RELATED LINKS</span></span>

[<span data-ttu-id="49710-138">Nowe — AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="49710-138">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="49710-139">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="49710-139">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)