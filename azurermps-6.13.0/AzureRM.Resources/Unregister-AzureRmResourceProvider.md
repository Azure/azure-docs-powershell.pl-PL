---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D5126B7B-7FBB-4C72-B77E-13ADE2BE9B1B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/unregister-azurermresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Unregister-AzureRmResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Unregister-AzureRmResourceProvider.md
ms.openlocfilehash: d957859fc03a5d8beec90190d473240acb7b2482
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718762"
---
# <span data-ttu-id="435c3-101">Unregister-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="435c3-101">Unregister-AzureRmResourceProvider</span></span>

## <span data-ttu-id="435c3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="435c3-102">SYNOPSIS</span></span>
<span data-ttu-id="435c3-103">Wyrejestrowuje dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="435c3-103">Unregisters a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="435c3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="435c3-104">SYNTAX</span></span>

```
Unregister-AzureRmResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="435c3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="435c3-105">DESCRIPTION</span></span>
<span data-ttu-id="435c3-106">Polecenie cmdlet **Unregister-AzureRmResourceProvider** wyrejestrowuje dostawcę zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="435c3-106">The **Unregister-AzureRmResourceProvider** cmdlet unregisters an Azure resource provider.</span></span>

## <span data-ttu-id="435c3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="435c3-107">EXAMPLES</span></span>

## <span data-ttu-id="435c3-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="435c3-108">PARAMETERS</span></span>

### <span data-ttu-id="435c3-109">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="435c3-109">-ApiVersion</span></span>
<span data-ttu-id="435c3-110">Określa wersję API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="435c3-110">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="435c3-111">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="435c3-111">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="435c3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="435c3-112">-DefaultProfile</span></span>
<span data-ttu-id="435c3-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="435c3-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="435c3-114">-Pre</span><span class="sxs-lookup"><span data-stu-id="435c3-114">-Pre</span></span>
<span data-ttu-id="435c3-115">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="435c3-115">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="435c3-116">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="435c3-116">-ProviderNamespace</span></span>
<span data-ttu-id="435c3-117">Określa obszar nazw dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="435c3-117">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="435c3-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="435c3-118">-Confirm</span></span>
<span data-ttu-id="435c3-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="435c3-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="435c3-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="435c3-120">-WhatIf</span></span>
<span data-ttu-id="435c3-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="435c3-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="435c3-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="435c3-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="435c3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="435c3-123">CommonParameters</span></span>
<span data-ttu-id="435c3-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="435c3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="435c3-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="435c3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="435c3-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="435c3-126">INPUTS</span></span>

## <span data-ttu-id="435c3-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="435c3-127">OUTPUTS</span></span>

## <span data-ttu-id="435c3-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="435c3-128">NOTES</span></span>

## <span data-ttu-id="435c3-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="435c3-129">RELATED LINKS</span></span>

[<span data-ttu-id="435c3-130">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="435c3-130">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="435c3-131">Rejestr — AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="435c3-131">Register-AzureRmResourceProvider</span></span>](./Register-AzureRmResourceProvider.md)


