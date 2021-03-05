---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
ms.openlocfilehash: 2937aafbcffd2444051b9bed0a764cb3aede6c52
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001050"
---
# <span data-ttu-id="992c9-101">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="992c9-101">Set-AzPublicIpPrefix</span></span>

## <span data-ttu-id="992c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="992c9-102">SYNOPSIS</span></span>
<span data-ttu-id="992c9-103">Ustawia tagi dla istniejącego publicipprefixu</span><span class="sxs-lookup"><span data-stu-id="992c9-103">Sets the Tags for an existing PublicIpPrefix</span></span>

## <span data-ttu-id="992c9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="992c9-104">SYNTAX</span></span>

```
Set-AzPublicIpPrefix -PublicIpPrefix <PSPublicIpPrefix> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="992c9-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="992c9-105">DESCRIPTION</span></span>
<span data-ttu-id="992c9-106">Polecenie **cmdlet Set-AzPublicIpPrefix** ustawia tagi dla publicznego prefiksu IP.</span><span class="sxs-lookup"><span data-stu-id="992c9-106">The **Set-AzPublicIpPrefix** cmdlet sets the Tags for a public IP prefix.</span></span>

## <span data-ttu-id="992c9-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="992c9-107">EXAMPLES</span></span>

### <span data-ttu-id="992c9-108">Ustawianie tagów dla publicznego prefiksu ip</span><span class="sxs-lookup"><span data-stu-id="992c9-108">Set the tags for public ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = Get-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName

PS C:\> $publicIpPrefix.Tags = "TestTag"

PS C:\> Set-AzPublicIpPrefix -PublicIpPrefix $publicIpPrefix
```

<span data-ttu-id="992c9-109">Pierwsze polecenie otrzymuje istniejący publiczny prefiks IP, drugie polecenie ustawia właściwość Tagi, a trzecie polecenie aktualizuje istniejący obiekt.</span><span class="sxs-lookup"><span data-stu-id="992c9-109">The first command gets an existing public IP Prefix, the second command sets the Tags Property and the third command updates the existing object.</span></span>

## <span data-ttu-id="992c9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="992c9-110">PARAMETERS</span></span>

### <span data-ttu-id="992c9-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="992c9-111">-AsJob</span></span>
<span data-ttu-id="992c9-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="992c9-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="992c9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="992c9-113">-DefaultProfile</span></span>
<span data-ttu-id="992c9-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="992c9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="992c9-115">- PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="992c9-115">-PublicIpPrefix</span></span>
<span data-ttu-id="992c9-116">The PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="992c9-116">The PublicIpPrefix</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="992c9-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="992c9-117">-Confirm</span></span>
<span data-ttu-id="992c9-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="992c9-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="992c9-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="992c9-119">-WhatIf</span></span>
<span data-ttu-id="992c9-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="992c9-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="992c9-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="992c9-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="992c9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="992c9-122">CommonParameters</span></span>
<span data-ttu-id="992c9-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="992c9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="992c9-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="992c9-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="992c9-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="992c9-125">INPUTS</span></span>

### <span data-ttu-id="992c9-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="992c9-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="992c9-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="992c9-127">OUTPUTS</span></span>

### <span data-ttu-id="992c9-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="992c9-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="992c9-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="992c9-129">NOTES</span></span>

## <span data-ttu-id="992c9-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="992c9-130">RELATED LINKS</span></span>

[<span data-ttu-id="992c9-131">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="992c9-131">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="992c9-132">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="992c9-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="992c9-133">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="992c9-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)
