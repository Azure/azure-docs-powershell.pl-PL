---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
ms.openlocfilehash: 347a05c5e197a93458a64c4079ce1fd430e631f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545843"
---
# <span data-ttu-id="ad203-101">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ad203-101">Remove-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="ad203-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ad203-102">SYNOPSIS</span></span>
<span data-ttu-id="ad203-103">Usuwanie wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ad203-103">Removes a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad203-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ad203-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad203-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ad203-105">DESCRIPTION</span></span>
<span data-ttu-id="ad203-106">Umożliwia usunięcie wewnętrznej bazy danych określonej przez identyfikator z funkcji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="ad203-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="ad203-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ad203-107">EXAMPLES</span></span>

### <span data-ttu-id="ad203-108">Przykład 1: usunięcie wewnętrznej bazy danych 123</span><span class="sxs-lookup"><span data-stu-id="ad203-108">Example 1: Remove the Backend 123</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="ad203-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ad203-109">PARAMETERS</span></span>

### <span data-ttu-id="ad203-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="ad203-110">-BackendId</span></span>
<span data-ttu-id="ad203-111">Identyfikator istniejącej wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ad203-111">Identifier of existing backend.</span></span>
<span data-ttu-id="ad203-112">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="ad203-112">This parameter is required.</span></span>

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

### <span data-ttu-id="ad203-113">-Context</span><span class="sxs-lookup"><span data-stu-id="ad203-113">-Context</span></span>
<span data-ttu-id="ad203-114">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="ad203-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ad203-115">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="ad203-115">This parameter is required.</span></span>

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

### <span data-ttu-id="ad203-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad203-116">-DefaultProfile</span></span>
<span data-ttu-id="ad203-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ad203-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="ad203-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad203-118">-PassThru</span></span>
<span data-ttu-id="ad203-119">Jeśli ta wartość zostanie określona, operacja ta zostanie zapisana jako prawda w przypadku powodzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="ad203-119">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="ad203-120">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="ad203-120">This parameter is optional.</span></span>
<span data-ttu-id="ad203-121">Wartość domyślna to false.</span><span class="sxs-lookup"><span data-stu-id="ad203-121">Default value is false.</span></span>

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

### <span data-ttu-id="ad203-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ad203-122">-Confirm</span></span>
<span data-ttu-id="ad203-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad203-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad203-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad203-124">-WhatIf</span></span>
<span data-ttu-id="ad203-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad203-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ad203-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ad203-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad203-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad203-127">CommonParameters</span></span>
<span data-ttu-id="ad203-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad203-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad203-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad203-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad203-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad203-130">INPUTS</span></span>

### <span data-ttu-id="ad203-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ad203-131">None</span></span>
<span data-ttu-id="ad203-132">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="ad203-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ad203-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ad203-133">OUTPUTS</span></span>

### <span data-ttu-id="ad203-134">logiczną</span><span class="sxs-lookup"><span data-stu-id="ad203-134">bool</span></span>

## <span data-ttu-id="ad203-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ad203-135">NOTES</span></span>

## <span data-ttu-id="ad203-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad203-136">RELATED LINKS</span></span>

[<span data-ttu-id="ad203-137">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ad203-137">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="ad203-138">Nowe — AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ad203-138">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="ad203-139">Nowe — AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="ad203-139">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="ad203-140">Nowe — AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="ad203-140">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="ad203-141">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ad203-141">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)
