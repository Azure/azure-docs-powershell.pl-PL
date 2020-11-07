---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 894297BF-2771-4871-9E4C-8684364DAC4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProperty.md
ms.openlocfilehash: ad6e2aebcc5a4edcf5acd3255385b0e78f317627
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704636"
---
# <span data-ttu-id="d060d-101">Get-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="d060d-101">Get-AzApiManagementProperty</span></span>

## <span data-ttu-id="d060d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d060d-102">SYNOPSIS</span></span>
<span data-ttu-id="d060d-103">Pobiera listę lub określoną właściwość (nazwa-wartość).</span><span class="sxs-lookup"><span data-stu-id="d060d-103">Gets a list or a particular Property (Named-Value).</span></span>

## <span data-ttu-id="d060d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d060d-104">SYNTAX</span></span>

### <span data-ttu-id="d060d-105">GetAllProperties (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d060d-105">GetAllProperties (Default)</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d060d-106">GetByPropertyId</span><span class="sxs-lookup"><span data-stu-id="d060d-106">GetByPropertyId</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d060d-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="d060d-107">GetByName</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d060d-108">GetByTag</span><span class="sxs-lookup"><span data-stu-id="d060d-108">GetByTag</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d060d-109">Opis</span><span class="sxs-lookup"><span data-stu-id="d060d-109">DESCRIPTION</span></span>
<span data-ttu-id="d060d-110">Polecenie cmdlet **Get-AzApiManagementProperty** pobiera listę lub określoną właściwość.</span><span class="sxs-lookup"><span data-stu-id="d060d-110">The **Get-AzApiManagementProperty** cmdlet gets a list or a particular property.</span></span>

## <span data-ttu-id="d060d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d060d-111">EXAMPLES</span></span>

### <span data-ttu-id="d060d-112">Przykład 1: pobieranie właściwości według nazwy</span><span class="sxs-lookup"><span data-stu-id="d060d-112">Example 1: Get Property by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProperty -Context $apimContext -Name "sql-connectionstring"
```

## <span data-ttu-id="d060d-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d060d-113">PARAMETERS</span></span>

### <span data-ttu-id="d060d-114">-Context</span><span class="sxs-lookup"><span data-stu-id="d060d-114">-Context</span></span>
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

### <span data-ttu-id="d060d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d060d-115">-DefaultProfile</span></span>
<span data-ttu-id="d060d-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d060d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d060d-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d060d-117">-Name</span></span>
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

### <span data-ttu-id="d060d-118">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="d060d-118">-PropertyId</span></span>
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

### <span data-ttu-id="d060d-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="d060d-119">-Tag</span></span>
<span data-ttu-id="d060d-120">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="d060d-120">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d060d-121">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="d060d-121">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d060d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d060d-122">CommonParameters</span></span>
<span data-ttu-id="d060d-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d060d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d060d-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d060d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d060d-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d060d-125">INPUTS</span></span>

### <span data-ttu-id="d060d-126">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d060d-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d060d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d060d-127">System.String</span></span>

## <span data-ttu-id="d060d-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d060d-128">OUTPUTS</span></span>

### <span data-ttu-id="d060d-129">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="d060d-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="d060d-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d060d-130">NOTES</span></span>

## <span data-ttu-id="d060d-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d060d-131">RELATED LINKS</span></span>