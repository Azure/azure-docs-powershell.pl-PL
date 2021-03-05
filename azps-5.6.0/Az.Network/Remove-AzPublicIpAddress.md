---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 00236BC2-61D8-49C2-91BE-923C567153F3
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpAddress.md
ms.openlocfilehash: f8a509fc73387361de5bd191ee9eefc61c33a5f9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996129"
---
# <span data-ttu-id="151c0-101">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="151c0-101">Remove-AzPublicIpAddress</span></span>

## <span data-ttu-id="151c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="151c0-102">SYNOPSIS</span></span>
<span data-ttu-id="151c0-103">Usuwa publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="151c0-103">Removes a public IP address.</span></span>

## <span data-ttu-id="151c0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="151c0-104">SYNTAX</span></span>

```
Remove-AzPublicIpAddress -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="151c0-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="151c0-105">DESCRIPTION</span></span>
<span data-ttu-id="151c0-106">Polecenie **cmdlet Remove-AzPublicIpAddress** usuwa publiczny adres IP platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="151c0-106">The **Remove-AzPublicIpAddress** cmdlet removes an Azure public IP address.</span></span>

## <span data-ttu-id="151c0-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="151c0-107">EXAMPLES</span></span>

### <span data-ttu-id="151c0-108">1. Usuwanie publicznego zasobu adresu IP</span><span class="sxs-lookup"><span data-stu-id="151c0-108">1: Remove a public IP address resource</span></span>
```
Remove-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="151c0-109">To polecenie usuwa publiczny zasób adresu IP o nazwie $publicIpName w grupie zasobów $rgName.</span><span class="sxs-lookup"><span data-stu-id="151c0-109">This command removes the public IP address resource named $publicIpName in the resource group $rgName.</span></span>

## <span data-ttu-id="151c0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="151c0-110">PARAMETERS</span></span>

### <span data-ttu-id="151c0-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="151c0-111">-AsJob</span></span>
<span data-ttu-id="151c0-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="151c0-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="151c0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="151c0-113">-DefaultProfile</span></span>
<span data-ttu-id="151c0-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="151c0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="151c0-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="151c0-115">-Force</span></span>
<span data-ttu-id="151c0-116">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="151c0-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="151c0-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="151c0-117">-Name</span></span>
<span data-ttu-id="151c0-118">Określa nazwę publicznego adresu IP, który usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="151c0-118">Specifies the name of the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="151c0-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="151c0-119">-PassThru</span></span>
<span data-ttu-id="151c0-120">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="151c0-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="151c0-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="151c0-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="151c0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="151c0-122">-ResourceGroupName</span></span>
<span data-ttu-id="151c0-123">Określa nazwę grupy zasobów zawierającą publiczny adres IP usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="151c0-123">Specifies the name of the resource group that contains the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="151c0-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="151c0-124">-Confirm</span></span>
<span data-ttu-id="151c0-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="151c0-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="151c0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="151c0-126">-WhatIf</span></span>
<span data-ttu-id="151c0-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="151c0-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="151c0-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="151c0-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="151c0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="151c0-129">CommonParameters</span></span>
<span data-ttu-id="151c0-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="151c0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="151c0-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="151c0-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="151c0-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="151c0-132">INPUTS</span></span>

### <span data-ttu-id="151c0-133">System.String</span><span class="sxs-lookup"><span data-stu-id="151c0-133">System.String</span></span>

## <span data-ttu-id="151c0-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="151c0-134">OUTPUTS</span></span>

### <span data-ttu-id="151c0-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="151c0-135">System.Boolean</span></span>

## <span data-ttu-id="151c0-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="151c0-136">NOTES</span></span>

## <span data-ttu-id="151c0-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="151c0-137">RELATED LINKS</span></span>

[<span data-ttu-id="151c0-138">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="151c0-138">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="151c0-139">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="151c0-139">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="151c0-140">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="151c0-140">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


