---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePortIdentity.md
ms.openlocfilehash: 330264eaaffd9d81da2ed8dbcc7c892477ffb7e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871087"
---
# <span data-ttu-id="7b648-101">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="7b648-101">Set-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="7b648-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7b648-102">SYNOPSIS</span></span>
<span data-ttu-id="7b648-103">Aktualizuje tożsamość przypisaną do ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="7b648-103">Updates a identity assigned to an ExpressRoutePort.</span></span>

## <span data-ttu-id="7b648-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7b648-104">SYNTAX</span></span>

```
Set-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort> -UserAssignedIdentityId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b648-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7b648-105">DESCRIPTION</span></span>
<span data-ttu-id="7b648-106">Polecenie cmdlet **Set-AzExpressRoutePortIdentity** umożliwia zaktualizowanie lokalnego obiektu usługi Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="7b648-106">The **Set-AzExpressRoutePortIdentity** cmdlet updates a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="7b648-107">Aby przypisać tę wartość do ExpressRoutePort, użyj **Ustawienia Set-AzExpressRoutePort** .</span><span class="sxs-lookup"><span data-stu-id="7b648-107">Use **Set-AzExpressRoutePort** to assign it to ExpressRoutePort.</span></span>

## <span data-ttu-id="7b648-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7b648-108">EXAMPLES</span></span>

### <span data-ttu-id="7b648-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7b648-109">Example 1</span></span>
```powershell
PS C:\>$exrport = Get-AzExpressRoutePort -Name $portName -ResourceGroupName $rgName
PS C:\>$identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\>$exrPortIdentity = Set-AzExpressRoutePortIdentity -UserAssignedIdentity $identity.Id -ExpressRoutePort $exrPort
PS C:\>$updatedExrPort = Set-AzExpressRoutePort -ExpressRoutePort $exrPort
```

## <span data-ttu-id="7b648-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7b648-110">PARAMETERS</span></span>

### <span data-ttu-id="7b648-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b648-111">-DefaultProfile</span></span>
<span data-ttu-id="7b648-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7b648-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b648-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7b648-113">-ExpressRoutePort</span></span>
<span data-ttu-id="7b648-114">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7b648-114">The ExpressRoutePort</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b648-115">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="7b648-115">-UserAssignedIdentityId</span></span>
<span data-ttu-id="7b648-116">Identyfikator ResourceId przypisanego użytkownikowi tożsamości, który ma zostać przypisany do ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="7b648-116">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: UserAssignedIdentity

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b648-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7b648-117">-Confirm</span></span>
<span data-ttu-id="7b648-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b648-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b648-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b648-119">-WhatIf</span></span>
<span data-ttu-id="7b648-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b648-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b648-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7b648-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b648-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b648-122">CommonParameters</span></span>
<span data-ttu-id="7b648-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b648-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b648-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b648-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b648-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7b648-125">INPUTS</span></span>

### <span data-ttu-id="7b648-126">Microsoft. Azure. Commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7b648-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="7b648-127">System. String</span><span class="sxs-lookup"><span data-stu-id="7b648-127">System.String</span></span>

## <span data-ttu-id="7b648-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7b648-128">OUTPUTS</span></span>

### <span data-ttu-id="7b648-129">Microsoft. Azure. Commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7b648-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="7b648-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7b648-130">NOTES</span></span>

## <span data-ttu-id="7b648-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7b648-131">RELATED LINKS</span></span>
[<span data-ttu-id="7b648-132">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="7b648-132">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="7b648-133">Nowe — AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="7b648-133">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="7b648-134">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="7b648-134">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)
