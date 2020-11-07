---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: F23D9274-63B9-4654-897B-6E84757774D2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApi.md
ms.openlocfilehash: 4bcda06e1c00e338feb80584fb6e2b51a63b051d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719210"
---
# <span data-ttu-id="2d4d5-101">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2d4d5-101">Remove-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="2d4d5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2d4d5-102">SYNOPSIS</span></span>
<span data-ttu-id="2d4d5-103">Usuwa interfejs API.</span><span class="sxs-lookup"><span data-stu-id="2d4d5-103">Removes an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d4d5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2d4d5-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d4d5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2d4d5-105">DESCRIPTION</span></span>
<span data-ttu-id="2d4d5-106">Polecenie cmdlet **Remove-AzureRmApiManagementApi** usuwa istniejący interfejs API.</span><span class="sxs-lookup"><span data-stu-id="2d4d5-106">The **Remove-AzureRmApiManagementApi** cmdlet removes an existing API.</span></span>

## <span data-ttu-id="2d4d5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2d4d5-107">EXAMPLES</span></span>

### <span data-ttu-id="2d4d5-108">Przykład 1: Usuwanie interfejsu API</span><span class="sxs-lookup"><span data-stu-id="2d4d5-108">Example 1: Remove an API</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApi -Context $apimContext -ApiId "0123456789"
```

<span data-ttu-id="2d4d5-109">To polecenie usuwa interfejs API o określonym IDENTYFIKATORze.</span><span class="sxs-lookup"><span data-stu-id="2d4d5-109">This command removes the API with the specified ID.</span></span>

## <span data-ttu-id="2d4d5-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2d4d5-110">PARAMETERS</span></span>

### <span data-ttu-id="2d4d5-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="2d4d5-111">-ApiId</span></span>
<span data-ttu-id="2d4d5-112">Określa identyfikator interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="2d4d5-112">Specifies the ID of the API remove.</span></span>

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

### <span data-ttu-id="2d4d5-113">-Context</span><span class="sxs-lookup"><span data-stu-id="2d4d5-113">-Context</span></span>
<span data-ttu-id="2d4d5-114">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="2d4d5-114">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d4d5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d4d5-115">-DefaultProfile</span></span>
<span data-ttu-id="2d4d5-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2d4d5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="2d4d5-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d4d5-117">-PassThru</span></span>
<span data-ttu-id="2d4d5-118">passthru</span><span class="sxs-lookup"><span data-stu-id="2d4d5-118">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d4d5-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2d4d5-119">-Confirm</span></span>
<span data-ttu-id="2d4d5-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d4d5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d4d5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d4d5-121">-WhatIf</span></span>
<span data-ttu-id="2d4d5-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d4d5-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d4d5-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2d4d5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d4d5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d4d5-124">CommonParameters</span></span>
<span data-ttu-id="2d4d5-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d4d5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d4d5-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d4d5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d4d5-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2d4d5-127">INPUTS</span></span>

### <span data-ttu-id="2d4d5-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="2d4d5-128">None</span></span>
<span data-ttu-id="2d4d5-129">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="2d4d5-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2d4d5-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2d4d5-130">OUTPUTS</span></span>

### <span data-ttu-id="2d4d5-131">Wartość</span><span class="sxs-lookup"><span data-stu-id="2d4d5-131">Boolean</span></span>

## <span data-ttu-id="2d4d5-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2d4d5-132">NOTES</span></span>

## <span data-ttu-id="2d4d5-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2d4d5-133">RELATED LINKS</span></span>

[<span data-ttu-id="2d4d5-134">Eksportowanie — AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2d4d5-134">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="2d4d5-135">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2d4d5-135">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="2d4d5-136">Import — AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2d4d5-136">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="2d4d5-137">Nowe — AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2d4d5-137">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="2d4d5-138">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2d4d5-138">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


