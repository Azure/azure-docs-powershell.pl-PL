---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterface.md
ms.openlocfilehash: f4de49bb2e35bf3d392fba06d663800a5bdc44a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184275"
---
# <span data-ttu-id="5bc1a-101">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="5bc1a-101">Remove-AzNetworkInterface</span></span>

## <span data-ttu-id="5bc1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bc1a-102">SYNOPSIS</span></span>
<span data-ttu-id="5bc1a-103">Usuwa interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="5bc1a-103">Removes a network interface.</span></span>

## <span data-ttu-id="5bc1a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5bc1a-104">SYNTAX</span></span>

```
Remove-AzNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bc1a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5bc1a-105">DESCRIPTION</span></span>
<span data-ttu-id="5bc1a-106">Polecenie **cmdlet Remove-AzNetworkInterface** usuwa interfejs sieciowy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5bc1a-106">The **Remove-AzNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="5bc1a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5bc1a-107">EXAMPLES</span></span>

### <span data-ttu-id="5bc1a-108">Przykład 1. Usuwanie interfejsu sieciowego</span><span class="sxs-lookup"><span data-stu-id="5bc1a-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="5bc1a-109">To polecenie usuwa interfejs sieciowy NetworkInterface1 w grupie zasobów ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="5bc1a-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="5bc1a-110">Ponieważ parametr *Force* nie jest używany, użytkownik zostanie wyświetlony monit o potwierdzenie tej akcji.</span><span class="sxs-lookup"><span data-stu-id="5bc1a-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="5bc1a-111">Przykład 2. Usuwanie interfejsu sieciowego</span><span class="sxs-lookup"><span data-stu-id="5bc1a-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzNetworkInterface -Force
```

<span data-ttu-id="5bc1a-112">To polecenie usuwa wszystkie interfejsy sieciowe w grupie zasobów ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="5bc1a-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="5bc1a-113">Parametr *Force jest* używany, dlatego użytkownik nie jest monitowany o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5bc1a-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="5bc1a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5bc1a-114">PARAMETERS</span></span>

### <span data-ttu-id="5bc1a-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="5bc1a-115">-AsJob</span></span>
<span data-ttu-id="5bc1a-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="5bc1a-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5bc1a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bc1a-117">-DefaultProfile</span></span>
<span data-ttu-id="5bc1a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5bc1a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5bc1a-119">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="5bc1a-119">-Force</span></span>
<span data-ttu-id="5bc1a-120">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="5bc1a-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5bc1a-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5bc1a-121">-Name</span></span>
<span data-ttu-id="5bc1a-122">Określa nazwę interfejsu sieciowego, który usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bc1a-122">Specifies the name of the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5bc1a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5bc1a-123">-PassThru</span></span>
<span data-ttu-id="5bc1a-124">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="5bc1a-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5bc1a-125">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="5bc1a-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5bc1a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bc1a-126">-ResourceGroupName</span></span>
<span data-ttu-id="5bc1a-127">Określa nazwę grupy zasobów zawierającej interfejs sieciowy usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bc1a-127">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5bc1a-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5bc1a-128">-Confirm</span></span>
<span data-ttu-id="5bc1a-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5bc1a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bc1a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bc1a-130">-WhatIf</span></span>
<span data-ttu-id="5bc1a-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bc1a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bc1a-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5bc1a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bc1a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bc1a-133">CommonParameters</span></span>
<span data-ttu-id="5bc1a-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bc1a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bc1a-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bc1a-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bc1a-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5bc1a-136">INPUTS</span></span>

### <span data-ttu-id="5bc1a-137">System.String</span><span class="sxs-lookup"><span data-stu-id="5bc1a-137">System.String</span></span>

## <span data-ttu-id="5bc1a-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5bc1a-138">OUTPUTS</span></span>

### <span data-ttu-id="5bc1a-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5bc1a-139">System.Boolean</span></span>

## <span data-ttu-id="5bc1a-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5bc1a-140">NOTES</span></span>

## <span data-ttu-id="5bc1a-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5bc1a-141">RELATED LINKS</span></span>

[<span data-ttu-id="5bc1a-142">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="5bc1a-142">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="5bc1a-143">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="5bc1a-143">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="5bc1a-144">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="5bc1a-144">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)


