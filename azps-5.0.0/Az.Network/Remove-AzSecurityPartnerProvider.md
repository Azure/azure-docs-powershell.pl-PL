---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzSecurityPartnerProvider.md
ms.openlocfilehash: a51345653580261178191687f54bf0f2a8cc6f0c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316981"
---
# <span data-ttu-id="ab363-101">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="ab363-101">Remove-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="ab363-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ab363-102">SYNOPSIS</span></span>
<span data-ttu-id="ab363-103">Usuwa usługę Azure SecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="ab363-103">Deletes an Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="ab363-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ab363-104">SYNTAX</span></span>

### <span data-ttu-id="ab363-105">SecurityPartnerProviderNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab363-105">SecurityPartnerProviderNameParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab363-106">SecurityPartnerProviderInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab363-106">SecurityPartnerProviderInputObjectParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -SecurityPartnerProvider <PSSecurityPartnerProvider> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab363-107">SecurityPartnerProviderResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab363-107">SecurityPartnerProviderResourceIdParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab363-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ab363-108">DESCRIPTION</span></span>
<span data-ttu-id="ab363-109">Polecenie cmdlet **Remove-AzSecurityPartnerProvider** usuwa składnik Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="ab363-109">The **Remove-AzSecurityPartnerProvider** cmdlet deletes an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="ab363-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ab363-110">EXAMPLES</span></span>

### <span data-ttu-id="ab363-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ab363-111">Example 1</span></span>
```powershell
Remove-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
```

## <span data-ttu-id="ab363-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ab363-112">PARAMETERS</span></span>

### <span data-ttu-id="ab363-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ab363-113">-AsJob</span></span>
<span data-ttu-id="ab363-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ab363-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ab363-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab363-115">-DefaultProfile</span></span>
<span data-ttu-id="ab363-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ab363-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab363-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ab363-117">-Force</span></span>
<span data-ttu-id="ab363-118">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ab363-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ab363-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ab363-119">-Name</span></span>
<span data-ttu-id="ab363-120">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="ab363-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab363-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ab363-121">-PassThru</span></span>
<span data-ttu-id="ab363-122">Zwraca obiekt reprezentujący element, dla którego wykonywana jest ta operacja.</span><span class="sxs-lookup"><span data-stu-id="ab363-122">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="ab363-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab363-123">-ResourceGroupName</span></span>
<span data-ttu-id="ab363-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ab363-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab363-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab363-125">-ResourceId</span></span>
<span data-ttu-id="ab363-126">Identyfikator zasobu securityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="ab363-126">The securityPartnerProvider resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab363-127">-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="ab363-127">-SecurityPartnerProvider</span></span>
<span data-ttu-id="ab363-128">Obiekt wejściowy securityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="ab363-128">The securityPartnerProvider input object.</span></span>

```yaml
Type: PSSecurityPartnerProvider
Parameter Sets: SecurityPartnerProviderInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab363-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ab363-129">-Confirm</span></span>
<span data-ttu-id="ab363-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab363-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab363-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab363-131">-WhatIf</span></span>
<span data-ttu-id="ab363-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab363-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab363-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ab363-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab363-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab363-134">CommonParameters</span></span>
<span data-ttu-id="ab363-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab363-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab363-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab363-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab363-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab363-137">INPUTS</span></span>

### <span data-ttu-id="ab363-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ab363-138">System.String</span></span>

### <span data-ttu-id="ab363-139">Microsoft. Azure. Commands. Network. models. PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="ab363-139">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="ab363-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ab363-140">OUTPUTS</span></span>

### <span data-ttu-id="ab363-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ab363-141">System.Boolean</span></span>

## <span data-ttu-id="ab363-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ab363-142">NOTES</span></span>

## <span data-ttu-id="ab363-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ab363-143">RELATED LINKS</span></span>
