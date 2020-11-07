---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/register-Azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Register-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Register-AzResourceProvider.md
ms.openlocfilehash: 7f9a5089e48da7c49716abe2bdbe710c0cf30e3b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892453"
---
# <span data-ttu-id="85f34-101">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="85f34-101">Register-AzResourceProvider</span></span>

## <span data-ttu-id="85f34-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="85f34-102">SYNOPSIS</span></span>
<span data-ttu-id="85f34-103">Rejestruje dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="85f34-103">Registers a resource provider.</span></span>

## <span data-ttu-id="85f34-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="85f34-104">SYNTAX</span></span>

```
Register-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85f34-105">Opis</span><span class="sxs-lookup"><span data-stu-id="85f34-105">DESCRIPTION</span></span>
<span data-ttu-id="85f34-106">Polecenie cmdlet **register-AzResourceProvider** rejestruje dostawcę zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="85f34-106">The **Register-AzResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="85f34-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="85f34-107">EXAMPLES</span></span>

### <span data-ttu-id="85f34-108">Przykład 1: rejestrowanie dostawcy</span><span class="sxs-lookup"><span data-stu-id="85f34-108">Example 1: Register a provider</span></span>
```
PS C:\>Register-AzResourceProvider -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="85f34-109">Spowoduje to zarejestrowanie dostawcy Microsoft. Network dla Twojego konta.</span><span class="sxs-lookup"><span data-stu-id="85f34-109">This registers the Microsoft.Network provider for your account.</span></span>

## <span data-ttu-id="85f34-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="85f34-110">PARAMETERS</span></span>

### <span data-ttu-id="85f34-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="85f34-111">-ApiVersion</span></span>
<span data-ttu-id="85f34-112">Określa wersję API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="85f34-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="85f34-113">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="85f34-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="85f34-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85f34-114">-DefaultProfile</span></span>
<span data-ttu-id="85f34-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="85f34-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85f34-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="85f34-116">-Pre</span></span>
<span data-ttu-id="85f34-117">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="85f34-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="85f34-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="85f34-118">-ProviderNamespace</span></span>
<span data-ttu-id="85f34-119">Określa obszar nazw dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="85f34-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="85f34-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="85f34-120">-Confirm</span></span>
<span data-ttu-id="85f34-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85f34-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85f34-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85f34-122">-WhatIf</span></span>
<span data-ttu-id="85f34-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85f34-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85f34-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="85f34-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85f34-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85f34-125">CommonParameters</span></span>
<span data-ttu-id="85f34-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85f34-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85f34-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85f34-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85f34-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85f34-128">INPUTS</span></span>

## <span data-ttu-id="85f34-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="85f34-129">OUTPUTS</span></span>

## <span data-ttu-id="85f34-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="85f34-130">NOTES</span></span>

## <span data-ttu-id="85f34-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="85f34-131">RELATED LINKS</span></span>

[<span data-ttu-id="85f34-132">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="85f34-132">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="85f34-133">Wyrejestrowanie — AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="85f34-133">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)


