---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: A4A8D996-72A2-4154-98DA-5F84CAA010B9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOperation.md
ms.openlocfilehash: ef3db99522c07b593493e30bd3778f1774af1a5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552287"
---
# <span data-ttu-id="5cbec-101">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="5cbec-101">Remove-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="5cbec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5cbec-102">SYNOPSIS</span></span>
<span data-ttu-id="5cbec-103">Usuwa istniejącą operację.</span><span class="sxs-lookup"><span data-stu-id="5cbec-103">Removes an existing operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5cbec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5cbec-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cbec-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5cbec-105">DESCRIPTION</span></span>
<span data-ttu-id="5cbec-106">Polecenie cmdlet **Remove-AzureRmApiManagementOperation** Usuwa istniejącą operację.</span><span class="sxs-lookup"><span data-stu-id="5cbec-106">The **Remove-AzureRmApiManagementOperation** cmdlet removes an existing operation.</span></span>

## <span data-ttu-id="5cbec-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5cbec-107">EXAMPLES</span></span>

### <span data-ttu-id="5cbec-108">Przykład 1. Usuń istniejącą operację interfejsu API</span><span class="sxs-lookup"><span data-stu-id="5cbec-108">Example 1: Remove an existing API Operation</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementOperation -Context $apimContext -ApiId "0123456789" -OperationId "9876543210" -Force
```

<span data-ttu-id="5cbec-109">To polecenie usuwa istniejącą operację interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="5cbec-109">This command removes an existing API Operation.</span></span>

## <span data-ttu-id="5cbec-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5cbec-110">PARAMETERS</span></span>

### <span data-ttu-id="5cbec-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="5cbec-111">-ApiId</span></span>
<span data-ttu-id="5cbec-112">Określa identyfikator interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="5cbec-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="5cbec-113">-Context</span><span class="sxs-lookup"><span data-stu-id="5cbec-113">-Context</span></span>
<span data-ttu-id="5cbec-114">Określa wystąpienie **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="5cbec-114">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="5cbec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cbec-115">-DefaultProfile</span></span>
<span data-ttu-id="5cbec-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5cbec-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="5cbec-117">-OperationId</span><span class="sxs-lookup"><span data-stu-id="5cbec-117">-OperationId</span></span>
<span data-ttu-id="5cbec-118">Określa identyfikator operacji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="5cbec-118">Specifies the identifier of the API operation.</span></span>

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

### <span data-ttu-id="5cbec-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5cbec-119">-PassThru</span></span>
<span data-ttu-id="5cbec-120">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli ta operacja się powiedzie lub wartość $False w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="5cbec-120">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="5cbec-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5cbec-121">-Confirm</span></span>
<span data-ttu-id="5cbec-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cbec-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cbec-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cbec-123">-WhatIf</span></span>
<span data-ttu-id="5cbec-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cbec-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cbec-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5cbec-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cbec-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cbec-126">CommonParameters</span></span>
<span data-ttu-id="5cbec-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cbec-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cbec-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cbec-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cbec-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5cbec-129">INPUTS</span></span>

### <span data-ttu-id="5cbec-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5cbec-130">None</span></span>
<span data-ttu-id="5cbec-131">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="5cbec-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5cbec-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5cbec-132">OUTPUTS</span></span>

### <span data-ttu-id="5cbec-133">logiczną</span><span class="sxs-lookup"><span data-stu-id="5cbec-133">bool</span></span>

## <span data-ttu-id="5cbec-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5cbec-134">NOTES</span></span>

## <span data-ttu-id="5cbec-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5cbec-135">RELATED LINKS</span></span>

[<span data-ttu-id="5cbec-136">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="5cbec-136">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="5cbec-137">Nowe — AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="5cbec-137">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="5cbec-138">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="5cbec-138">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


