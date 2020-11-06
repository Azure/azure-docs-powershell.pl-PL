---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: CD582654-1B0C-4960-9E18-454F857B56E7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagement.md
ms.openlocfilehash: 197b1605d178c0aaa1c3f96580cb295306910232
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553060"
---
# <span data-ttu-id="0384a-101">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="0384a-101">Remove-AzureRmApiManagement</span></span>

## <span data-ttu-id="0384a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0384a-102">SYNOPSIS</span></span>
<span data-ttu-id="0384a-103">Usuwa usługę zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="0384a-103">Removes an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0384a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0384a-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0384a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0384a-105">DESCRIPTION</span></span>
<span data-ttu-id="0384a-106">Polecenie cmdlet **Remove-AzureRmApiManagement** usuwa usługę zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="0384a-106">The **Remove-AzureRmApiManagement** cmdlet removes an Azure API Management service.</span></span>

## <span data-ttu-id="0384a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0384a-107">EXAMPLES</span></span>

### <span data-ttu-id="0384a-108">Przykład 1: Usuwanie usługi zarządzania interfejsem API</span><span class="sxs-lookup"><span data-stu-id="0384a-108">Example 1: Remove an API Management service</span></span>
```
PS C:\>Remove-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi"
```

<span data-ttu-id="0384a-109">To polecenie usuwa usługę zarządzania interfejsem API o nazwie ContosoApi.</span><span class="sxs-lookup"><span data-stu-id="0384a-109">This command removes the API Management service named ContosoApi.</span></span>

## <span data-ttu-id="0384a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0384a-110">PARAMETERS</span></span>

### <span data-ttu-id="0384a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0384a-111">-DefaultProfile</span></span>
<span data-ttu-id="0384a-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0384a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="0384a-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0384a-113">-Name</span></span>
<span data-ttu-id="0384a-114">Określa nazwę wdrożenia zarządzania interfejsem API, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0384a-114">Specifies the name of the API Management deployment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0384a-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0384a-115">-PassThru</span></span>
<span data-ttu-id="0384a-116">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli operacja się powiedzie.</span><span class="sxs-lookup"><span data-stu-id="0384a-116">Indicates that this cmdlet returns a value of $True if the operation succeeds.</span></span>

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

### <span data-ttu-id="0384a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0384a-117">-ResourceGroupName</span></span>
<span data-ttu-id="0384a-118">Określa nazwę grupy zasobów, w której istnieje wdrożenie zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="0384a-118">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="0384a-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0384a-119">-Confirm</span></span>
<span data-ttu-id="0384a-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0384a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0384a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0384a-121">-WhatIf</span></span>
<span data-ttu-id="0384a-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0384a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0384a-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0384a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0384a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0384a-124">CommonParameters</span></span>
<span data-ttu-id="0384a-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0384a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0384a-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0384a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0384a-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0384a-127">INPUTS</span></span>

### <span data-ttu-id="0384a-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="0384a-128">None</span></span>
<span data-ttu-id="0384a-129">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="0384a-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0384a-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0384a-130">OUTPUTS</span></span>

### <span data-ttu-id="0384a-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0384a-131">System.Boolean</span></span>

## <span data-ttu-id="0384a-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0384a-132">NOTES</span></span>

## <span data-ttu-id="0384a-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0384a-133">RELATED LINKS</span></span>

[<span data-ttu-id="0384a-134">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="0384a-134">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="0384a-135">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="0384a-135">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="0384a-136">Nowe — AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="0384a-136">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="0384a-137">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="0384a-137">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


