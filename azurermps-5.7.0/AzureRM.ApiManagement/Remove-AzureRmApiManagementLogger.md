---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 98AD1C84-B147-48EB-94B5-8D77B531F6F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementLogger.md
ms.openlocfilehash: 2dbd515877e44023077d782080cff29d78a0e6fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553707"
---
# <span data-ttu-id="78ea5-101">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="78ea5-101">Remove-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="78ea5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="78ea5-102">SYNOPSIS</span></span>
<span data-ttu-id="78ea5-103">Usuwa rejestratora zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="78ea5-103">Removes an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78ea5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="78ea5-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78ea5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="78ea5-105">DESCRIPTION</span></span>
<span data-ttu-id="78ea5-106">Polecenie cmdlet **Remove-AzureRmApiManagementLogger** usuwa **Rejestrator** zarządzania interfejsem API platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="78ea5-106">The **Remove-AzureRmApiManagementLogger** cmdlet removes an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="78ea5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="78ea5-107">EXAMPLES</span></span>

### <span data-ttu-id="78ea5-108">Przykład 1: usuwanie rejestratora</span><span class="sxs-lookup"><span data-stu-id="78ea5-108">Example 1: Remove a logger</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Force
```

<span data-ttu-id="78ea5-109">To polecenie usuwa rejestratora o IDENTYFIKATORze Logger123.</span><span class="sxs-lookup"><span data-stu-id="78ea5-109">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="78ea5-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="78ea5-110">PARAMETERS</span></span>

### <span data-ttu-id="78ea5-111">-Context</span><span class="sxs-lookup"><span data-stu-id="78ea5-111">-Context</span></span>
<span data-ttu-id="78ea5-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="78ea5-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="78ea5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78ea5-113">-DefaultProfile</span></span>
<span data-ttu-id="78ea5-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="78ea5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="78ea5-115">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="78ea5-115">-LoggerId</span></span>
<span data-ttu-id="78ea5-116">Określa identyfikator rejestratora, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="78ea5-116">Specifies the ID of the logger to remove.</span></span>

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

### <span data-ttu-id="78ea5-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78ea5-117">-PassThru</span></span>
<span data-ttu-id="78ea5-118">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli operacja się powiedzie lub $False w inny sposób.</span><span class="sxs-lookup"><span data-stu-id="78ea5-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="78ea5-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="78ea5-119">-Confirm</span></span>
<span data-ttu-id="78ea5-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78ea5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78ea5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78ea5-121">-WhatIf</span></span>
<span data-ttu-id="78ea5-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78ea5-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78ea5-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="78ea5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78ea5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78ea5-124">CommonParameters</span></span>
<span data-ttu-id="78ea5-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78ea5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78ea5-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78ea5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78ea5-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78ea5-127">INPUTS</span></span>

### <span data-ttu-id="78ea5-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="78ea5-128">None</span></span>
<span data-ttu-id="78ea5-129">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="78ea5-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="78ea5-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="78ea5-130">OUTPUTS</span></span>

### <span data-ttu-id="78ea5-131">Wartość</span><span class="sxs-lookup"><span data-stu-id="78ea5-131">Boolean</span></span>

## <span data-ttu-id="78ea5-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="78ea5-132">NOTES</span></span>

## <span data-ttu-id="78ea5-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="78ea5-133">RELATED LINKS</span></span>

[<span data-ttu-id="78ea5-134">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="78ea5-134">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="78ea5-135">Nowe — AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="78ea5-135">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="78ea5-136">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="78ea5-136">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


