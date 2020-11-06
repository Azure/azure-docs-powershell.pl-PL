---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmResourceProvider.md
ms.openlocfilehash: 92d94950bc4bc90494482b22b81cbd918c8b6938
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549876"
---
# <span data-ttu-id="ca43d-101">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="ca43d-101">Register-AzureRmResourceProvider</span></span>

## <span data-ttu-id="ca43d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ca43d-102">SYNOPSIS</span></span>
<span data-ttu-id="ca43d-103">Rejestruje dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="ca43d-103">Registers a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca43d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ca43d-104">SYNTAX</span></span>

```
Register-AzureRmResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca43d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ca43d-105">DESCRIPTION</span></span>
<span data-ttu-id="ca43d-106">Polecenie cmdlet **register-AzureRmResourceProvider** rejestruje dostawcę zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ca43d-106">The **Register-AzureRmResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="ca43d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ca43d-107">EXAMPLES</span></span>

## <span data-ttu-id="ca43d-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ca43d-108">PARAMETERS</span></span>

### <span data-ttu-id="ca43d-109">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ca43d-109">-ApiVersion</span></span>
<span data-ttu-id="ca43d-110">Określa wersję API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="ca43d-110">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="ca43d-111">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="ca43d-111">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="ca43d-112">-Pre</span><span class="sxs-lookup"><span data-stu-id="ca43d-112">-Pre</span></span>
<span data-ttu-id="ca43d-113">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="ca43d-113">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ca43d-114">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="ca43d-114">-ProviderNamespace</span></span>
<span data-ttu-id="ca43d-115">Określa obszar nazw dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ca43d-115">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="ca43d-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ca43d-116">-Confirm</span></span>
<span data-ttu-id="ca43d-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca43d-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca43d-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca43d-118">-WhatIf</span></span>
<span data-ttu-id="ca43d-119">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca43d-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca43d-120">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ca43d-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca43d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca43d-121">-DefaultProfile</span></span>
<span data-ttu-id="ca43d-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ca43d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca43d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca43d-123">CommonParameters</span></span>
<span data-ttu-id="ca43d-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca43d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca43d-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca43d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca43d-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ca43d-126">INPUTS</span></span>

## <span data-ttu-id="ca43d-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ca43d-127">OUTPUTS</span></span>

### <span data-ttu-id="ca43d-128">Microsoft. Azure. Commands. resourceName. polecenia. cmdlet. SdkModels. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="ca43d-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="ca43d-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ca43d-129">NOTES</span></span>

## <span data-ttu-id="ca43d-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ca43d-130">RELATED LINKS</span></span>

[<span data-ttu-id="ca43d-131">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="ca43d-131">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="ca43d-132">Wyrejestrowanie — AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="ca43d-132">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)


