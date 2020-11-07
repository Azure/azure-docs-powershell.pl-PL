---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/register-azurermresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmResourceProvider.md
ms.openlocfilehash: 9e379df74f974e303faac300515e6bb7844e770b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717696"
---
# <span data-ttu-id="97e3b-101">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="97e3b-101">Register-AzureRmResourceProvider</span></span>

## <span data-ttu-id="97e3b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="97e3b-102">SYNOPSIS</span></span>
<span data-ttu-id="97e3b-103">Rejestruje dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="97e3b-103">Registers a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97e3b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="97e3b-104">SYNTAX</span></span>

```
Register-AzureRmResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97e3b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="97e3b-105">DESCRIPTION</span></span>
<span data-ttu-id="97e3b-106">Polecenie cmdlet **register-AzureRmResourceProvider** rejestruje dostawcę zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="97e3b-106">The **Register-AzureRmResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="97e3b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="97e3b-107">EXAMPLES</span></span>

### <span data-ttu-id="97e3b-108">Przykład 1: rejestrowanie dostawcy</span><span class="sxs-lookup"><span data-stu-id="97e3b-108">Example 1: Register a provider</span></span>
```
PS C:\>Register-AzureRmResourceProvider -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="97e3b-109">Spowoduje to zarejestrowanie dostawcy Microsoft. Network dla Twojego konta.</span><span class="sxs-lookup"><span data-stu-id="97e3b-109">This registers the Microsoft.Network provider for your account.</span></span>

## <span data-ttu-id="97e3b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="97e3b-110">PARAMETERS</span></span>

### <span data-ttu-id="97e3b-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="97e3b-111">-ApiVersion</span></span>
<span data-ttu-id="97e3b-112">Określa wersję API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="97e3b-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="97e3b-113">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="97e3b-113">You can specify a different version than the default version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97e3b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97e3b-114">-DefaultProfile</span></span>
<span data-ttu-id="97e3b-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="97e3b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97e3b-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="97e3b-116">-Pre</span></span>
<span data-ttu-id="97e3b-117">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="97e3b-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="97e3b-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="97e3b-118">-ProviderNamespace</span></span>
<span data-ttu-id="97e3b-119">Określa obszar nazw dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="97e3b-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="97e3b-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="97e3b-120">-Confirm</span></span>
<span data-ttu-id="97e3b-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97e3b-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97e3b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97e3b-122">-WhatIf</span></span>
<span data-ttu-id="97e3b-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97e3b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97e3b-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="97e3b-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97e3b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97e3b-125">CommonParameters</span></span>
<span data-ttu-id="97e3b-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97e3b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97e3b-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97e3b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97e3b-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="97e3b-128">INPUTS</span></span>

### <span data-ttu-id="97e3b-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="97e3b-129">None</span></span>
<span data-ttu-id="97e3b-130">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="97e3b-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="97e3b-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="97e3b-131">OUTPUTS</span></span>

### <span data-ttu-id="97e3b-132">Microsoft. Azure. Commands. resourceName. polecenia. cmdlet. SdkModels. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="97e3b-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="97e3b-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="97e3b-133">NOTES</span></span>

## <span data-ttu-id="97e3b-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="97e3b-134">RELATED LINKS</span></span>

[<span data-ttu-id="97e3b-135">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="97e3b-135">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="97e3b-136">Wyrejestrowanie — AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="97e3b-136">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)


