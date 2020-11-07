---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
ms.openlocfilehash: caa0baf8e26ea2cec94a59bd2a86e6394b4ade91
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708945"
---
# <span data-ttu-id="08455-101">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="08455-101">Set-AzPublicIpPrefix</span></span>

## <span data-ttu-id="08455-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="08455-102">SYNOPSIS</span></span>
<span data-ttu-id="08455-103">Ustawia znaczniki dla istniejącej PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="08455-103">Sets the Tags for an existing PublicIpPrefix</span></span>

## <span data-ttu-id="08455-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="08455-104">SYNTAX</span></span>

```
Set-AzPublicIpPrefix -PublicIpPrefix <PSPublicIpPrefix> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08455-105">Opis</span><span class="sxs-lookup"><span data-stu-id="08455-105">DESCRIPTION</span></span>
<span data-ttu-id="08455-106">Polecenie cmdlet **Set-AzPublicIpPrefix** ustawia znaczniki dla publicznego PREFIKSU adresu IP.</span><span class="sxs-lookup"><span data-stu-id="08455-106">The **Set-AzPublicIpPrefix** cmdlet sets the Tags for a public IP prefix.</span></span>

## <span data-ttu-id="08455-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="08455-107">EXAMPLES</span></span>

### <span data-ttu-id="08455-108">Ustawianie tagów publicznego prefiksu adresu IP</span><span class="sxs-lookup"><span data-stu-id="08455-108">Set the tags for public ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = Get-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName

PS C:\> $publicIpPrefix.Tags = "TestTag"

PS C:\> Set-AzPublicIpPrefix -PublicIpPrefix $publicIpPrefix
```

<span data-ttu-id="08455-109">Pierwsze polecenie pobiera istniejący publiczny prefiks IP, drugie polecenie ustawia właściwość Tagi, a trzecie polecenie aktualizuje istniejący obiekt.</span><span class="sxs-lookup"><span data-stu-id="08455-109">The first command gets an existing public IP Prefix, the second command sets the Tags Property and the third command updates the existing object.</span></span>

## <span data-ttu-id="08455-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="08455-110">PARAMETERS</span></span>

### <span data-ttu-id="08455-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="08455-111">-AsJob</span></span>
<span data-ttu-id="08455-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="08455-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="08455-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08455-113">-DefaultProfile</span></span>
<span data-ttu-id="08455-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="08455-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08455-115">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="08455-115">-PublicIpPrefix</span></span>
<span data-ttu-id="08455-116">PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="08455-116">The PublicIpPrefix</span></span>

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

### <span data-ttu-id="08455-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="08455-117">-Confirm</span></span>
<span data-ttu-id="08455-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08455-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08455-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08455-119">-WhatIf</span></span>
<span data-ttu-id="08455-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08455-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08455-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="08455-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08455-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08455-122">CommonParameters</span></span>
<span data-ttu-id="08455-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08455-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08455-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08455-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08455-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="08455-125">INPUTS</span></span>

### <span data-ttu-id="08455-126">Microsoft. Azure. Commands. Network. models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="08455-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="08455-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="08455-127">OUTPUTS</span></span>

### <span data-ttu-id="08455-128">Microsoft. Azure. Commands. Network. models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="08455-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="08455-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="08455-129">NOTES</span></span>

## <span data-ttu-id="08455-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="08455-130">RELATED LINKS</span></span>

[<span data-ttu-id="08455-131">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="08455-131">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="08455-132">Nowe — AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="08455-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="08455-133">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="08455-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)
