---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 894297BF-2771-4871-9E4C-8684364DAC4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
ms.openlocfilehash: 7542e9621d90ffdb19bb8db679592dd17a216d5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717249"
---
# <span data-ttu-id="ea356-101">Get-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="ea356-101">Get-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="ea356-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ea356-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea356-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ea356-103">SYNTAX</span></span>

### <span data-ttu-id="ea356-104">Pobieranie wszystkich właściwości (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="ea356-104">Get all properties (Default)</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ea356-105">Identyfikator właściwości</span><span class="sxs-lookup"><span data-stu-id="ea356-105">Get by property ID</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea356-106">Znajdowanie właściwości zawierających nazwę</span><span class="sxs-lookup"><span data-stu-id="ea356-106">Find properties containing Name</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea356-107">Znajdowanie właściwości według tagu</span><span class="sxs-lookup"><span data-stu-id="ea356-107">Find properties by Tag</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea356-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ea356-108">DESCRIPTION</span></span>

## <span data-ttu-id="ea356-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ea356-109">EXAMPLES</span></span>

### <span data-ttu-id="ea356-110">1:1</span><span class="sxs-lookup"><span data-stu-id="ea356-110">1:</span></span>
```
PS C:\> Get-AzureRmApiManagementProperty -Context $Context -Name $PropertyName
```

## <span data-ttu-id="ea356-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ea356-111">PARAMETERS</span></span>

### <span data-ttu-id="ea356-112">-Context</span><span class="sxs-lookup"><span data-stu-id="ea356-112">-Context</span></span>
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

### <span data-ttu-id="ea356-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ea356-113">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: Find properties containing Name
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea356-114">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="ea356-114">-PropertyId</span></span>
```yaml
Type: System.String
Parameter Sets: Get by property ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea356-115">-Tag</span><span class="sxs-lookup"><span data-stu-id="ea356-115">-Tag</span></span>
<span data-ttu-id="ea356-116">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="ea356-116">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ea356-117">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="ea356-117">For example:</span></span>

<span data-ttu-id="ea356-118">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="ea356-118">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.String
Parameter Sets: Find properties by Tag
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea356-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea356-119">-DefaultProfile</span></span>
<span data-ttu-id="ea356-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ea356-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea356-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea356-121">CommonParameters</span></span>
<span data-ttu-id="ea356-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea356-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea356-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea356-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea356-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea356-124">INPUTS</span></span>

## <span data-ttu-id="ea356-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ea356-125">OUTPUTS</span></span>

### <span data-ttu-id="ea356-126">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. ApiManagement. servicemanagement. modele. PsApiManagementProperty]</span><span class="sxs-lookup"><span data-stu-id="ea356-126">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty]</span></span>

### <span data-ttu-id="ea356-127">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="ea356-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="ea356-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ea356-128">NOTES</span></span>

## <span data-ttu-id="ea356-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ea356-129">RELATED LINKS</span></span>

