---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzRouteFilter.md
ms.openlocfilehash: 02f3e0a151fe8dc810e8530af88059371139f08c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892929"
---
# <span data-ttu-id="376b3-101">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="376b3-101">Remove-AzRouteFilter</span></span>

## <span data-ttu-id="376b3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="376b3-102">SYNOPSIS</span></span>
<span data-ttu-id="376b3-103">{{Wpisz w postaci streszczenia}}</span><span class="sxs-lookup"><span data-stu-id="376b3-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="376b3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="376b3-104">SYNTAX</span></span>

```
Remove-AzRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="376b3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="376b3-105">DESCRIPTION</span></span>
<span data-ttu-id="376b3-106">{{Wpisz opis}}</span><span class="sxs-lookup"><span data-stu-id="376b3-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="376b3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="376b3-107">EXAMPLES</span></span>

### <span data-ttu-id="376b3-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="376b3-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="376b3-109">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="376b3-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="376b3-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="376b3-110">PARAMETERS</span></span>

### <span data-ttu-id="376b3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="376b3-111">-DefaultProfile</span></span>
<span data-ttu-id="376b3-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="376b3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="376b3-113">-Force</span><span class="sxs-lookup"><span data-stu-id="376b3-113">-Force</span></span>
<span data-ttu-id="376b3-114">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="376b3-114">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="376b3-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="376b3-115">-Name</span></span>
<span data-ttu-id="376b3-116">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="376b3-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="376b3-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="376b3-117">-PassThru</span></span>
<span data-ttu-id="376b3-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="376b3-118">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="376b3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="376b3-119">-ResourceGroupName</span></span>
<span data-ttu-id="376b3-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="376b3-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="376b3-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="376b3-121">-Confirm</span></span>
<span data-ttu-id="376b3-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="376b3-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="376b3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="376b3-123">-WhatIf</span></span>
<span data-ttu-id="376b3-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="376b3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="376b3-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="376b3-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="376b3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="376b3-126">CommonParameters</span></span>
<span data-ttu-id="376b3-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="376b3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="376b3-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="376b3-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="376b3-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="376b3-129">INPUTS</span></span>

### <span data-ttu-id="376b3-130">System. String</span><span class="sxs-lookup"><span data-stu-id="376b3-130">System.String</span></span>

## <span data-ttu-id="376b3-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="376b3-131">OUTPUTS</span></span>

### <span data-ttu-id="376b3-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="376b3-132">System.Object</span></span>

## <span data-ttu-id="376b3-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="376b3-133">NOTES</span></span>

## <span data-ttu-id="376b3-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="376b3-134">RELATED LINKS</span></span>

