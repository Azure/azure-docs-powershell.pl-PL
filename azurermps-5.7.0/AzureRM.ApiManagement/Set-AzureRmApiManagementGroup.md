---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
ms.openlocfilehash: 20f2f79c154cd16dcf09501bdbefb488fdeb61eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545836"
---
# <span data-ttu-id="5e579-101">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="5e579-101">Set-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="5e579-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5e579-102">SYNOPSIS</span></span>
<span data-ttu-id="5e579-103">Umożliwia skonfigurowanie grupy zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="5e579-103">Configures an API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e579-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5e579-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e579-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5e579-105">DESCRIPTION</span></span>
<span data-ttu-id="5e579-106">Polecenie cmdlet **Set-AzureRmApiManagementGroup** umożliwia skonfigurowanie grupy zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="5e579-106">The **Set-AzureRmApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="5e579-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5e579-107">EXAMPLES</span></span>

### <span data-ttu-id="5e579-108">Przykład 1: Konfigurowanie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="5e579-108">Example 1: Configure a management group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementGroup -Context $apimContext -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="5e579-109">To polecenie umożliwia skonfigurowanie grupy zarządzania o nazwie Group0001.</span><span class="sxs-lookup"><span data-stu-id="5e579-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="5e579-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5e579-110">PARAMETERS</span></span>

### <span data-ttu-id="5e579-111">-Context</span><span class="sxs-lookup"><span data-stu-id="5e579-111">-Context</span></span>
<span data-ttu-id="5e579-112">Określa wystąpienie obiektu **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="5e579-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="5e579-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e579-113">-DefaultProfile</span></span>
<span data-ttu-id="5e579-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5e579-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="5e579-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="5e579-115">-Description</span></span>
<span data-ttu-id="5e579-116">Określa opis grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="5e579-116">Specifies the description of the management group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e579-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="5e579-117">-GroupId</span></span>
<span data-ttu-id="5e579-118">Określa identyfikator grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="5e579-118">Specifies the identifier of the management group.</span></span>

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

### <span data-ttu-id="5e579-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5e579-119">-Name</span></span>
<span data-ttu-id="5e579-120">Określa nazwę grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="5e579-120">Specifies the name of the management group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e579-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e579-121">-PassThru</span></span>
<span data-ttu-id="5e579-122">passthru</span><span class="sxs-lookup"><span data-stu-id="5e579-122">passthru</span></span>

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

### <span data-ttu-id="5e579-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e579-123">CommonParameters</span></span>
<span data-ttu-id="5e579-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e579-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e579-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e579-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e579-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5e579-126">INPUTS</span></span>

### <span data-ttu-id="5e579-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5e579-127">None</span></span>
<span data-ttu-id="5e579-128">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="5e579-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5e579-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5e579-129">OUTPUTS</span></span>

### <span data-ttu-id="5e579-130">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="5e579-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="5e579-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5e579-131">NOTES</span></span>

## <span data-ttu-id="5e579-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5e579-132">RELATED LINKS</span></span>

[<span data-ttu-id="5e579-133">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="5e579-133">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="5e579-134">Nowe — AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="5e579-134">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="5e579-135">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="5e579-135">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)


