---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: https://docs.microsoft.com/powershell/module/az.network/remove-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterface.md
ms.openlocfilehash: 54bc4a3b9875f68df8a7c824c7e4f754e6f35a4e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993651"
---
# <span data-ttu-id="76734-101">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="76734-101">Remove-AzNetworkInterface</span></span>

## <span data-ttu-id="76734-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76734-102">SYNOPSIS</span></span>
<span data-ttu-id="76734-103">Usuwa interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="76734-103">Removes a network interface.</span></span>

## <span data-ttu-id="76734-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="76734-104">SYNTAX</span></span>

```
Remove-AzNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76734-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="76734-105">DESCRIPTION</span></span>
<span data-ttu-id="76734-106">Polecenie **cmdlet Remove-AzNetworkInterface** usuwa interfejs sieciowy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="76734-106">The **Remove-AzNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="76734-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="76734-107">EXAMPLES</span></span>

### <span data-ttu-id="76734-108">Przykład 1. Usuwanie interfejsu sieciowego</span><span class="sxs-lookup"><span data-stu-id="76734-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="76734-109">To polecenie usuwa interfejs sieciowy NetworkInterface1 w grupie zasobów ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="76734-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="76734-110">Ponieważ parametr *Force* nie jest używany, użytkownik zostanie wyświetlony monit o potwierdzenie tej akcji.</span><span class="sxs-lookup"><span data-stu-id="76734-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="76734-111">Przykład 2. Usuwanie interfejsu sieciowego</span><span class="sxs-lookup"><span data-stu-id="76734-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzNetworkInterface -Force
```

<span data-ttu-id="76734-112">To polecenie usuwa wszystkie interfejsy sieciowe w grupie zasobów ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="76734-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="76734-113">Parametr *Force jest* używany, dlatego użytkownik nie jest monitowany o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="76734-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="76734-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76734-114">PARAMETERS</span></span>

### <span data-ttu-id="76734-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="76734-115">-AsJob</span></span>
<span data-ttu-id="76734-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="76734-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="76734-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76734-117">-DefaultProfile</span></span>
<span data-ttu-id="76734-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="76734-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76734-119">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="76734-119">-Force</span></span>
<span data-ttu-id="76734-120">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="76734-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="76734-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="76734-121">-Name</span></span>
<span data-ttu-id="76734-122">Określa nazwę interfejsu sieciowego, który usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76734-122">Specifies the name of the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="76734-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="76734-123">-PassThru</span></span>
<span data-ttu-id="76734-124">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="76734-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="76734-125">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="76734-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="76734-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76734-126">-ResourceGroupName</span></span>
<span data-ttu-id="76734-127">Określa nazwę grupy zasobów zawierającej interfejs sieciowy usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76734-127">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="76734-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="76734-128">-Confirm</span></span>
<span data-ttu-id="76734-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="76734-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76734-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76734-130">-WhatIf</span></span>
<span data-ttu-id="76734-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76734-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76734-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="76734-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76734-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76734-133">CommonParameters</span></span>
<span data-ttu-id="76734-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76734-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76734-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76734-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76734-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76734-136">INPUTS</span></span>

### <span data-ttu-id="76734-137">System.String</span><span class="sxs-lookup"><span data-stu-id="76734-137">System.String</span></span>

## <span data-ttu-id="76734-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76734-138">OUTPUTS</span></span>

### <span data-ttu-id="76734-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="76734-139">System.Boolean</span></span>

## <span data-ttu-id="76734-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="76734-140">NOTES</span></span>

## <span data-ttu-id="76734-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="76734-141">RELATED LINKS</span></span>

[<span data-ttu-id="76734-142">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="76734-142">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="76734-143">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="76734-143">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="76734-144">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="76734-144">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)


