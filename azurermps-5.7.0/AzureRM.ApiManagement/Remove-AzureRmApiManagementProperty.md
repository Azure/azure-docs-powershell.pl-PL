---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: D3C60123-CE1F-45F1-8C8F-25CDC302490C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProperty.md
ms.openlocfilehash: d8c47cb6aaf1f135cd08110f4ab1d616cb105f15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525393"
---
# <span data-ttu-id="edbab-101">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="edbab-101">Remove-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="edbab-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="edbab-102">SYNOPSIS</span></span>
<span data-ttu-id="edbab-103">Usuwa Właściwość zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="edbab-103">Removes an API Management Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="edbab-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="edbab-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edbab-105">Opis</span><span class="sxs-lookup"><span data-stu-id="edbab-105">DESCRIPTION</span></span>
<span data-ttu-id="edbab-106">Polecenie cmdlet **Remove-AzureRmApiManagementProperty** usuwa **Właściwość** zarządzanie interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="edbab-106">The **Remove-AzureRmApiManagementProperty** cmdlet removes an Azure API Management **Property**.</span></span>

## <span data-ttu-id="edbab-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="edbab-107">EXAMPLES</span></span>

### <span data-ttu-id="edbab-108">Przykład 1. Usuń właściwość</span><span class="sxs-lookup"><span data-stu-id="edbab-108">Example 1: Remove a property</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property11" -PassThru
```

<span data-ttu-id="edbab-109">To polecenie usuwa właściwość o IDENTYFIKATORze Property11.</span><span class="sxs-lookup"><span data-stu-id="edbab-109">This command removes the property that has the ID Property11.</span></span>

## <span data-ttu-id="edbab-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="edbab-110">PARAMETERS</span></span>

### <span data-ttu-id="edbab-111">-Context</span><span class="sxs-lookup"><span data-stu-id="edbab-111">-Context</span></span>
<span data-ttu-id="edbab-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="edbab-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="edbab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edbab-113">-DefaultProfile</span></span>
<span data-ttu-id="edbab-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="edbab-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="edbab-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="edbab-115">-PassThru</span></span>
<span data-ttu-id="edbab-116">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli operacja się powiedzie lub $False w inny sposób.</span><span class="sxs-lookup"><span data-stu-id="edbab-116">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="edbab-117">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="edbab-117">-PropertyId</span></span>
<span data-ttu-id="edbab-118">Określa identyfikator właściwości, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edbab-118">Specifies an ID of the property that this cmdlet removes.</span></span>

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

### <span data-ttu-id="edbab-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="edbab-119">-Confirm</span></span>
<span data-ttu-id="edbab-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edbab-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edbab-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edbab-121">-WhatIf</span></span>
<span data-ttu-id="edbab-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edbab-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edbab-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="edbab-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edbab-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edbab-124">CommonParameters</span></span>
<span data-ttu-id="edbab-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edbab-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edbab-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edbab-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edbab-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="edbab-127">INPUTS</span></span>

### <span data-ttu-id="edbab-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="edbab-128">None</span></span>
<span data-ttu-id="edbab-129">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="edbab-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="edbab-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="edbab-130">OUTPUTS</span></span>

### <span data-ttu-id="edbab-131">logiczną</span><span class="sxs-lookup"><span data-stu-id="edbab-131">bool</span></span>

## <span data-ttu-id="edbab-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="edbab-132">NOTES</span></span>

## <span data-ttu-id="edbab-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="edbab-133">RELATED LINKS</span></span>

[<span data-ttu-id="edbab-134">Nowe — AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="edbab-134">New-AzureRmApiManagementProperty</span></span>](./New-AzureRmApiManagementProperty.md)

[<span data-ttu-id="edbab-135">Set-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="edbab-135">Set-AzureRmApiManagementProperty</span></span>](./Set-AzureRmApiManagementProperty.md)


