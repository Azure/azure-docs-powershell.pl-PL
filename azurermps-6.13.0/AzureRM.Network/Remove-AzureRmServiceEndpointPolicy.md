---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmServiceEndpointPolicy.md
ms.openlocfilehash: f3871e23c0d193ef2ea89c43e3a30c5597abbfe0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552663"
---
# <span data-ttu-id="d3375-101">Remove-AzureRmServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d3375-101">Remove-AzureRmServiceEndpointPolicy</span></span>

## <span data-ttu-id="d3375-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d3375-102">SYNOPSIS</span></span>
<span data-ttu-id="d3375-103">{{Wpisz w postaci streszczenia}}</span><span class="sxs-lookup"><span data-stu-id="d3375-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3375-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d3375-104">SYNTAX</span></span>

```
Remove-AzureRmServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3375-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d3375-105">DESCRIPTION</span></span>
<span data-ttu-id="d3375-106">Polecenie cmdlet **Remove-AzureRmServiceEndpointPolicy** usuwa zasadę punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="d3375-106">The **Remove-AzureRmServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="d3375-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d3375-107">EXAMPLES</span></span>

### <span data-ttu-id="d3375-108">Przykład 1. usuwa zasadę punktu końcowego usługi przy użyciu nazwy</span><span class="sxs-lookup"><span data-stu-id="d3375-108">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzureRmServiceEndpointPolicy -Name "Policy1" -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="d3375-109">To polecenie usuwa zasadę punktu końcowego usługi o nazwie Policy1 należącej do źródła danych o nazwie "resourcegroup1".</span><span class="sxs-lookup"><span data-stu-id="d3375-109">This command removes a service endpoint policy with name Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

### <span data-ttu-id="d3375-110">Przykład 2: usuwanie zasad punktu końcowego usługi za pomocą obiektu wejściowego</span><span class="sxs-lookup"><span data-stu-id="d3375-110">Example 2: Remove a service endpoint policy using input object</span></span>
```
Remove-AzureRmServiceEndpointPolicy -InputObject $Policy1 -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="d3375-111">To polecenie usuwa obiekt zasad punktu końcowego usługi Policy1, który należy do obiektu resourceName o nazwie "resourcegroup1".</span><span class="sxs-lookup"><span data-stu-id="d3375-111">This command removes a service endpoint policy object Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

## <span data-ttu-id="d3375-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d3375-112">PARAMETERS</span></span>

### <span data-ttu-id="d3375-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3375-113">-DefaultProfile</span></span>
<span data-ttu-id="d3375-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d3375-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3375-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d3375-115">-Force</span></span>
<span data-ttu-id="d3375-116">Nie pytaj o potwierdzenie, czy zachodzi konieczność przestania się zasobu</span><span class="sxs-lookup"><span data-stu-id="d3375-116">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="d3375-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d3375-117">-Name</span></span>
<span data-ttu-id="d3375-118">Nazwa zasad punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="d3375-118">The name of the service endpoint policy</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3375-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3375-119">-PassThru</span></span>
<span data-ttu-id="d3375-120">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d3375-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d3375-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3375-121">-ResourceGroupName</span></span>
<span data-ttu-id="d3375-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d3375-122">The resource group name.</span></span>

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

### <span data-ttu-id="d3375-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d3375-123">-Confirm</span></span>
<span data-ttu-id="d3375-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3375-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3375-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3375-125">-WhatIf</span></span>
<span data-ttu-id="d3375-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3375-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3375-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d3375-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3375-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3375-128">CommonParameters</span></span>
<span data-ttu-id="d3375-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3375-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d3375-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3375-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3375-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d3375-131">INPUTS</span></span>

### <span data-ttu-id="d3375-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d3375-132">System.String</span></span>


## <span data-ttu-id="d3375-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d3375-133">OUTPUTS</span></span>

### <span data-ttu-id="d3375-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="d3375-134">System.Object</span></span>

## <span data-ttu-id="d3375-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d3375-135">NOTES</span></span>

## <span data-ttu-id="d3375-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d3375-136">RELATED LINKS</span></span>
