---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E9390015-FD5C-4015-BA81-3445ADF8F8BF
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
ms.openlocfilehash: 7095190570e649ab5262de0a8cebfc97d55fbf17
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984298"
---
# <span data-ttu-id="7a27d-101">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7a27d-101">Remove-AzApplicationGateway</span></span>

## <span data-ttu-id="7a27d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a27d-102">SYNOPSIS</span></span>
<span data-ttu-id="7a27d-103">Usuwa bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7a27d-103">Removes an application gateway.</span></span>

## <span data-ttu-id="7a27d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7a27d-104">SYNTAX</span></span>

```
Remove-AzApplicationGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a27d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="7a27d-105">DESCRIPTION</span></span>
<span data-ttu-id="7a27d-106">Polecenie **cmdlet Remove-AzApplicationGateway** usuwa bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7a27d-106">The **Remove-AzApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="7a27d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7a27d-107">EXAMPLES</span></span>

### <span data-ttu-id="7a27d-108">Przykład 1. Usuwanie określonej bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="7a27d-108">Example 1: Remove a specified application gateway</span></span>
```
PS C:\>Remove-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="7a27d-109">To polecenie usuwa bramę aplikacji o nazwie ApplicationGateway01 z grupy zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="7a27d-109">This command removes the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="7a27d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a27d-110">PARAMETERS</span></span>

### <span data-ttu-id="7a27d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a27d-111">-DefaultProfile</span></span>
<span data-ttu-id="7a27d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7a27d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a27d-113">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="7a27d-113">-Force</span></span>
<span data-ttu-id="7a27d-114">Wskazuje, że polecenie cmdlet wymusza usunięcie bramy aplikacji, niezależnie od tego, czy zasoby są do niego przypisane.</span><span class="sxs-lookup"><span data-stu-id="7a27d-114">Indicates that the cmdlet forces the deletion of the application gateway regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="7a27d-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7a27d-115">-Name</span></span>
<span data-ttu-id="7a27d-116">Określa nazwę bramy aplikacji do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="7a27d-116">Specifies the name of the application gateway to be removed.</span></span>

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

### <span data-ttu-id="7a27d-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a27d-117">-PassThru</span></span>
<span data-ttu-id="7a27d-118">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="7a27d-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7a27d-119">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="7a27d-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7a27d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a27d-120">-ResourceGroupName</span></span>
<span data-ttu-id="7a27d-121">Określa nazwę grupy zasobów, do której należy brama aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7a27d-121">Specifies the name of the resource group name that the application gateway belongs to.</span></span>

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

### <span data-ttu-id="7a27d-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7a27d-122">-Confirm</span></span>
<span data-ttu-id="7a27d-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7a27d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a27d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a27d-124">-WhatIf</span></span>
<span data-ttu-id="7a27d-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a27d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a27d-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7a27d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a27d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a27d-127">CommonParameters</span></span>
<span data-ttu-id="7a27d-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a27d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a27d-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a27d-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a27d-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a27d-130">INPUTS</span></span>

### <span data-ttu-id="7a27d-131">System.String</span><span class="sxs-lookup"><span data-stu-id="7a27d-131">System.String</span></span>

### <span data-ttu-id="7a27d-132">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="7a27d-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7a27d-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a27d-133">OUTPUTS</span></span>

### <span data-ttu-id="7a27d-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7a27d-134">System.Boolean</span></span>

## <span data-ttu-id="7a27d-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7a27d-135">NOTES</span></span>

## <span data-ttu-id="7a27d-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7a27d-136">RELATED LINKS</span></span>

[<span data-ttu-id="7a27d-137">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7a27d-137">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)


