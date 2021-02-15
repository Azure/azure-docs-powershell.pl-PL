---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
ms.openlocfilehash: 4244f8c97090009272933d73a64323e4af5dfbbf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189450"
---
# <span data-ttu-id="d9928-101">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d9928-101">Set-AzPublicIpPrefix</span></span>

## <span data-ttu-id="d9928-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9928-102">SYNOPSIS</span></span>
<span data-ttu-id="d9928-103">Ustawia tagi dla istniejącego publicipprefixu</span><span class="sxs-lookup"><span data-stu-id="d9928-103">Sets the Tags for an existing PublicIpPrefix</span></span>

## <span data-ttu-id="d9928-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d9928-104">SYNTAX</span></span>

```
Set-AzPublicIpPrefix -PublicIpPrefix <PSPublicIpPrefix> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9928-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d9928-105">DESCRIPTION</span></span>
<span data-ttu-id="d9928-106">Polecenie **cmdlet Set-AzPublicIpPrefix** ustawia tagi dla publicznego prefiksu IP.</span><span class="sxs-lookup"><span data-stu-id="d9928-106">The **Set-AzPublicIpPrefix** cmdlet sets the Tags for a public IP prefix.</span></span>

## <span data-ttu-id="d9928-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d9928-107">EXAMPLES</span></span>

### <span data-ttu-id="d9928-108">Ustawianie tagów dla publicznego prefiksu ip</span><span class="sxs-lookup"><span data-stu-id="d9928-108">Set the tags for public ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = Get-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName

PS C:\> $publicIpPrefix.Tags = "TestTag"

PS C:\> Set-AzPublicIpPrefix -PublicIpPrefix $publicIpPrefix
```

<span data-ttu-id="d9928-109">Pierwsze polecenie otrzymuje istniejący publiczny prefiks IP, drugie polecenie ustawia właściwość Tagi, a trzecie polecenie aktualizuje istniejący obiekt.</span><span class="sxs-lookup"><span data-stu-id="d9928-109">The first command gets an existing public IP Prefix, the second command sets the Tags Property and the third command updates the existing object.</span></span>

## <span data-ttu-id="d9928-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9928-110">PARAMETERS</span></span>

### <span data-ttu-id="d9928-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d9928-111">-AsJob</span></span>
<span data-ttu-id="d9928-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d9928-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d9928-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9928-113">-DefaultProfile</span></span>
<span data-ttu-id="d9928-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d9928-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9928-115">- PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d9928-115">-PublicIpPrefix</span></span>
<span data-ttu-id="d9928-116">The PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d9928-116">The PublicIpPrefix</span></span>

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

### <span data-ttu-id="d9928-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d9928-117">-Confirm</span></span>
<span data-ttu-id="d9928-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d9928-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9928-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9928-119">-WhatIf</span></span>
<span data-ttu-id="d9928-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9928-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9928-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d9928-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9928-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9928-122">CommonParameters</span></span>
<span data-ttu-id="d9928-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9928-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9928-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9928-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9928-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9928-125">INPUTS</span></span>

### <span data-ttu-id="d9928-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d9928-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="d9928-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9928-127">OUTPUTS</span></span>

### <span data-ttu-id="d9928-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d9928-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="d9928-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d9928-129">NOTES</span></span>

## <span data-ttu-id="d9928-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d9928-130">RELATED LINKS</span></span>

[<span data-ttu-id="d9928-131">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d9928-131">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="d9928-132">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d9928-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="d9928-133">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d9928-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)
