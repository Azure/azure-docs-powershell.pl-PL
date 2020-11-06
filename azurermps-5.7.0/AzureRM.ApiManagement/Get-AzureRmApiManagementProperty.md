---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 894297BF-2771-4871-9E4C-8684364DAC4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
ms.openlocfilehash: 47167e0729ab3476c74124e16d6ae95901f57ad2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544599"
---
# <span data-ttu-id="9362a-101">Get-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="9362a-101">Get-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="9362a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9362a-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9362a-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9362a-103">SYNTAX</span></span>

### <span data-ttu-id="9362a-104">GetAllProperties (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9362a-104">GetAllProperties (Default)</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9362a-105">GetByPropertyId</span><span class="sxs-lookup"><span data-stu-id="9362a-105">GetByPropertyId</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9362a-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="9362a-106">GetByName</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9362a-107">GetByTag</span><span class="sxs-lookup"><span data-stu-id="9362a-107">GetByTag</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9362a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9362a-108">DESCRIPTION</span></span>

## <span data-ttu-id="9362a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9362a-109">EXAMPLES</span></span>

### <span data-ttu-id="9362a-110">Przykład 1: pobieranie właściwości według nazwy</span><span class="sxs-lookup"><span data-stu-id="9362a-110">Example 1: Get Property by name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementProperty -Context $apimContext -Name "sql-connectionstring"
```

## <span data-ttu-id="9362a-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9362a-111">PARAMETERS</span></span>

### <span data-ttu-id="9362a-112">-Context</span><span class="sxs-lookup"><span data-stu-id="9362a-112">-Context</span></span>
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

### <span data-ttu-id="9362a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9362a-113">-DefaultProfile</span></span>
<span data-ttu-id="9362a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9362a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="9362a-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9362a-115">-Name</span></span>
```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9362a-116">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="9362a-116">-PropertyId</span></span>
```yaml
Type: String
Parameter Sets: GetByPropertyId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9362a-117">-Tag</span><span class="sxs-lookup"><span data-stu-id="9362a-117">-Tag</span></span>
<span data-ttu-id="9362a-118">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="9362a-118">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9362a-119">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="9362a-119">For example:</span></span>

<span data-ttu-id="9362a-120">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="9362a-120">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: String
Parameter Sets: GetByTag
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9362a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9362a-121">CommonParameters</span></span>
<span data-ttu-id="9362a-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9362a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9362a-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9362a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9362a-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9362a-124">INPUTS</span></span>

### <span data-ttu-id="9362a-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9362a-125">None</span></span>
<span data-ttu-id="9362a-126">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="9362a-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9362a-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9362a-127">OUTPUTS</span></span>

### <span data-ttu-id="9362a-128">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. ApiManagement. servicemanagement. modele. PsApiManagementProperty]</span><span class="sxs-lookup"><span data-stu-id="9362a-128">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty]</span></span>

### <span data-ttu-id="9362a-129">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="9362a-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="9362a-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9362a-130">NOTES</span></span>

## <span data-ttu-id="9362a-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9362a-131">RELATED LINKS</span></span>

