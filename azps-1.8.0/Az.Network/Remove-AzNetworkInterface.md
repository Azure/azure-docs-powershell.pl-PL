---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterface.md
ms.openlocfilehash: 61cae1140ef0c46eee5857c15d0b6032a65caeb0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709113"
---
# <span data-ttu-id="d164e-101">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d164e-101">Remove-AzNetworkInterface</span></span>

## <span data-ttu-id="d164e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d164e-102">SYNOPSIS</span></span>
<span data-ttu-id="d164e-103">Usuwa interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="d164e-103">Removes a network interface.</span></span>

## <span data-ttu-id="d164e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d164e-104">SYNTAX</span></span>

```
Remove-AzNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d164e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d164e-105">DESCRIPTION</span></span>
<span data-ttu-id="d164e-106">Polecenie cmdlet **Remove-AzNetworkInterface** Usuwa interfejs sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="d164e-106">The **Remove-AzNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="d164e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d164e-107">EXAMPLES</span></span>

### <span data-ttu-id="d164e-108">Przykład 1: Usuwanie interfejsu sieciowego</span><span class="sxs-lookup"><span data-stu-id="d164e-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="d164e-109">To polecenie usuwa kartę Network Interface NetworkInterface1 w ResourceGroup1 Group (zasób).</span><span class="sxs-lookup"><span data-stu-id="d164e-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="d164e-110">Ponieważ parametr *Force* nie jest wykorzystywany, użytkownik zostanie poproszony o potwierdzenie tej akcji.</span><span class="sxs-lookup"><span data-stu-id="d164e-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="d164e-111">Przykład 2: Usuwanie interfejsu sieciowego</span><span class="sxs-lookup"><span data-stu-id="d164e-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzNetworkInterface -Force
```

<span data-ttu-id="d164e-112">To polecenie usuwa wszystkie interfejsy sieciowe w ResourceGroup1 grup zasobów.</span><span class="sxs-lookup"><span data-stu-id="d164e-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="d164e-113">Ponieważ parametr *Force* jest wykorzystywany, użytkownik nie jest monitowany o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d164e-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="d164e-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d164e-114">PARAMETERS</span></span>

### <span data-ttu-id="d164e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d164e-115">-AsJob</span></span>
<span data-ttu-id="d164e-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d164e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d164e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d164e-117">-DefaultProfile</span></span>
<span data-ttu-id="d164e-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d164e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d164e-119">-Force</span><span class="sxs-lookup"><span data-stu-id="d164e-119">-Force</span></span>
<span data-ttu-id="d164e-120">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d164e-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d164e-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d164e-121">-Name</span></span>
<span data-ttu-id="d164e-122">Określa nazwę interfejsu sieciowego, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d164e-122">Specifies the name of the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d164e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d164e-123">-PassThru</span></span>
<span data-ttu-id="d164e-124">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="d164e-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d164e-125">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="d164e-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d164e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d164e-126">-ResourceGroupName</span></span>
<span data-ttu-id="d164e-127">Określa nazwę grupy zasobów zawierającej interfejs sieciowy, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d164e-127">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d164e-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d164e-128">-Confirm</span></span>
<span data-ttu-id="d164e-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d164e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d164e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d164e-130">-WhatIf</span></span>
<span data-ttu-id="d164e-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d164e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d164e-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d164e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d164e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d164e-133">CommonParameters</span></span>
<span data-ttu-id="d164e-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d164e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d164e-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d164e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d164e-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d164e-136">INPUTS</span></span>

### <span data-ttu-id="d164e-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d164e-137">System.String</span></span>

## <span data-ttu-id="d164e-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d164e-138">OUTPUTS</span></span>

### <span data-ttu-id="d164e-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d164e-139">System.Boolean</span></span>

## <span data-ttu-id="d164e-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d164e-140">NOTES</span></span>

## <span data-ttu-id="d164e-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d164e-141">RELATED LINKS</span></span>

[<span data-ttu-id="d164e-142">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d164e-142">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="d164e-143">Nowe — AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d164e-143">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="d164e-144">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d164e-144">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)


