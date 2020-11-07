---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D5126B7B-7FBB-4C72-B77E-13ADE2BE9B1B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/unregister-azurermresourceprovider
schema: 2.0.0
ms.openlocfilehash: ead0edddccc5372c04e2e4b77d7860bbad29c27a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898177"
---
# <span data-ttu-id="c33b8-101">Unregister-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="c33b8-101">Unregister-AzureRmResourceProvider</span></span>

## <span data-ttu-id="c33b8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c33b8-102">SYNOPSIS</span></span>
<span data-ttu-id="c33b8-103">Wyrejestrowuje dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="c33b8-103">Unregisters a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c33b8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c33b8-104">SYNTAX</span></span>

```
Unregister-AzureRmResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c33b8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c33b8-105">DESCRIPTION</span></span>
<span data-ttu-id="c33b8-106">Polecenie cmdlet **Unregister-AzureRmResourceProvider** wyrejestrowuje dostawcę zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c33b8-106">The **Unregister-AzureRmResourceProvider** cmdlet unregisters an Azure resource provider.</span></span>

## <span data-ttu-id="c33b8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c33b8-107">EXAMPLES</span></span>

## <span data-ttu-id="c33b8-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c33b8-108">PARAMETERS</span></span>

### <span data-ttu-id="c33b8-109">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c33b8-109">-ApiVersion</span></span>
<span data-ttu-id="c33b8-110">Określa wersję API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="c33b8-110">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="c33b8-111">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="c33b8-111">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c33b8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c33b8-112">-DefaultProfile</span></span>
<span data-ttu-id="c33b8-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c33b8-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c33b8-114">-Pre</span><span class="sxs-lookup"><span data-stu-id="c33b8-114">-Pre</span></span>
<span data-ttu-id="c33b8-115">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="c33b8-115">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c33b8-116">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="c33b8-116">-ProviderNamespace</span></span>
<span data-ttu-id="c33b8-117">Określa obszar nazw dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c33b8-117">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="c33b8-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c33b8-118">-Confirm</span></span>
<span data-ttu-id="c33b8-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c33b8-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c33b8-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c33b8-120">-WhatIf</span></span>
<span data-ttu-id="c33b8-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c33b8-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c33b8-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c33b8-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c33b8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c33b8-123">CommonParameters</span></span>
<span data-ttu-id="c33b8-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c33b8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c33b8-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c33b8-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c33b8-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c33b8-126">INPUTS</span></span>

## <span data-ttu-id="c33b8-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c33b8-127">OUTPUTS</span></span>

## <span data-ttu-id="c33b8-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c33b8-128">NOTES</span></span>

## <span data-ttu-id="c33b8-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c33b8-129">RELATED LINKS</span></span>

[<span data-ttu-id="c33b8-130">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="c33b8-130">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="c33b8-131">Rejestr — AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="c33b8-131">Register-AzureRmResourceProvider</span></span>](./Register-AzureRmResourceProvider.md)


