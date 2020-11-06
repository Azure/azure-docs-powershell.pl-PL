---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteFilter.md
ms.openlocfilehash: 3f7e0a96212e9de87c90cffd059801084da471ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545028"
---
# <span data-ttu-id="03055-101">Remove-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="03055-101">Remove-AzureRmRouteFilter</span></span>

## <span data-ttu-id="03055-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="03055-102">SYNOPSIS</span></span>
<span data-ttu-id="03055-103">{{Wpisz w postaci streszczenia}}</span><span class="sxs-lookup"><span data-stu-id="03055-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03055-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="03055-104">SYNTAX</span></span>

```
Remove-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03055-105">Opis</span><span class="sxs-lookup"><span data-stu-id="03055-105">DESCRIPTION</span></span>
<span data-ttu-id="03055-106">{{Wpisz opis}}</span><span class="sxs-lookup"><span data-stu-id="03055-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="03055-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="03055-107">EXAMPLES</span></span>

### <span data-ttu-id="03055-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="03055-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="03055-109">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="03055-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="03055-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="03055-110">PARAMETERS</span></span>

### <span data-ttu-id="03055-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03055-111">-DefaultProfile</span></span>
<span data-ttu-id="03055-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="03055-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03055-113">-Force</span><span class="sxs-lookup"><span data-stu-id="03055-113">-Force</span></span>
<span data-ttu-id="03055-114">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="03055-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="03055-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="03055-115">-Name</span></span>
<span data-ttu-id="03055-116">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="03055-116">The resource name.</span></span>

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

### <span data-ttu-id="03055-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03055-117">-PassThru</span></span>
<span data-ttu-id="03055-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="03055-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="03055-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03055-119">-ResourceGroupName</span></span>
<span data-ttu-id="03055-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="03055-120">The resource group name.</span></span>

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

### <span data-ttu-id="03055-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="03055-121">-Confirm</span></span>
<span data-ttu-id="03055-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03055-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03055-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03055-123">-WhatIf</span></span>
<span data-ttu-id="03055-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03055-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03055-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="03055-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03055-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03055-126">CommonParameters</span></span>
<span data-ttu-id="03055-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03055-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03055-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03055-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03055-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03055-129">INPUTS</span></span>

### <span data-ttu-id="03055-130">System. String</span><span class="sxs-lookup"><span data-stu-id="03055-130">System.String</span></span>

## <span data-ttu-id="03055-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="03055-131">OUTPUTS</span></span>

### <span data-ttu-id="03055-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="03055-132">System.Boolean</span></span>

## <span data-ttu-id="03055-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="03055-133">NOTES</span></span>

## <span data-ttu-id="03055-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03055-134">RELATED LINKS</span></span>
