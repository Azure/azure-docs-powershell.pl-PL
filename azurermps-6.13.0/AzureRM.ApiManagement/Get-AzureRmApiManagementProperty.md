---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 894297BF-2771-4871-9E4C-8684364DAC4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
ms.openlocfilehash: 22cba1b904032ee654b091d1adae541848fd50c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524741"
---
# <span data-ttu-id="393f8-101">Get-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="393f8-101">Get-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="393f8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="393f8-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="393f8-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="393f8-103">SYNTAX</span></span>

### <span data-ttu-id="393f8-104">GetAllProperties (domyślny)</span><span class="sxs-lookup"><span data-stu-id="393f8-104">GetAllProperties (Default)</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="393f8-105">GetByPropertyId</span><span class="sxs-lookup"><span data-stu-id="393f8-105">GetByPropertyId</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="393f8-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="393f8-106">GetByName</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="393f8-107">GetByTag</span><span class="sxs-lookup"><span data-stu-id="393f8-107">GetByTag</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="393f8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="393f8-108">DESCRIPTION</span></span>

## <span data-ttu-id="393f8-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="393f8-109">EXAMPLES</span></span>

### <span data-ttu-id="393f8-110">Przykład 1: pobieranie właściwości według nazwy</span><span class="sxs-lookup"><span data-stu-id="393f8-110">Example 1: Get Property by name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementProperty -Context $apimContext -Name "sql-connectionstring"
```

## <span data-ttu-id="393f8-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="393f8-111">PARAMETERS</span></span>

### <span data-ttu-id="393f8-112">-Context</span><span class="sxs-lookup"><span data-stu-id="393f8-112">-Context</span></span>
```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="393f8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="393f8-113">-DefaultProfile</span></span>
<span data-ttu-id="393f8-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="393f8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="393f8-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="393f8-115">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="393f8-116">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="393f8-116">-PropertyId</span></span>
```yaml
Type: System.String
Parameter Sets: GetByPropertyId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="393f8-117">-Tag</span><span class="sxs-lookup"><span data-stu-id="393f8-117">-Tag</span></span>
<span data-ttu-id="393f8-118">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="393f8-118">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="393f8-119">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="393f8-119">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.String
Parameter Sets: GetByTag
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="393f8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="393f8-120">CommonParameters</span></span>
<span data-ttu-id="393f8-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="393f8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="393f8-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="393f8-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="393f8-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="393f8-123">INPUTS</span></span>

### <span data-ttu-id="393f8-124">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="393f8-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="393f8-125">System. String</span><span class="sxs-lookup"><span data-stu-id="393f8-125">System.String</span></span>

## <span data-ttu-id="393f8-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="393f8-126">OUTPUTS</span></span>

### <span data-ttu-id="393f8-127">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="393f8-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="393f8-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="393f8-128">NOTES</span></span>

## <span data-ttu-id="393f8-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="393f8-129">RELATED LINKS</span></span>
