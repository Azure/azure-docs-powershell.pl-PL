---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 3B5FC8E3-5A02-4F3B-81F0-51DFE47A201B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementTenantAccess.md
ms.openlocfilehash: 55158ac4f6489d70e17008c9e8c4ef13bd6d4fe0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719204"
---
# <span data-ttu-id="3161b-101">Set-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="3161b-101">Set-AzureRmApiManagementTenantAccess</span></span>

## <span data-ttu-id="3161b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3161b-102">SYNOPSIS</span></span>
<span data-ttu-id="3161b-103">Włącza lub wyłącza dostęp dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="3161b-103">Enables or disables tenant access.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3161b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3161b-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementTenantAccess -Context <PsApiManagementContext> -Enabled <Boolean> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3161b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3161b-105">DESCRIPTION</span></span>
<span data-ttu-id="3161b-106">Polecenie cmdlet **Set-AzureRmApiManagementTenantAccess** włącza lub wyłącza dostęp dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="3161b-106">The **Set-AzureRmApiManagementTenantAccess** cmdlet enables or disables tenant access.</span></span>

## <span data-ttu-id="3161b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3161b-107">EXAMPLES</span></span>

### <span data-ttu-id="3161b-108">Przykład 1: Włączanie dostępu do dzierżawy</span><span class="sxs-lookup"><span data-stu-id="3161b-108">Example 1: Enable tenant access</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementTenantAccess -Context $apimContext -Enabled $True
```

<span data-ttu-id="3161b-109">To polecenie umożliwia dostęp dzierżawy w określonym kontekście.</span><span class="sxs-lookup"><span data-stu-id="3161b-109">This command enables tenant access in the specified context.</span></span>

## <span data-ttu-id="3161b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3161b-110">PARAMETERS</span></span>

### <span data-ttu-id="3161b-111">-Context</span><span class="sxs-lookup"><span data-stu-id="3161b-111">-Context</span></span>
<span data-ttu-id="3161b-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="3161b-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3161b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3161b-113">-DefaultProfile</span></span>
<span data-ttu-id="3161b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3161b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="3161b-115">-Enabled</span><span class="sxs-lookup"><span data-stu-id="3161b-115">-Enabled</span></span>
<span data-ttu-id="3161b-116">Określa, czy to polecenie cmdlet włącza lub wyłącza dostęp dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="3161b-116">Specifies whether this cmdlet enables or disables tenant access.</span></span>
<span data-ttu-id="3161b-117">Określ wartość $True, aby włączyć lub $False wyłączyć.</span><span class="sxs-lookup"><span data-stu-id="3161b-117">Specify a value of $True to enable or $False to disable.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3161b-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3161b-118">-PassThru</span></span>
<span data-ttu-id="3161b-119">Wskazuje, że to polecenie cmdlet zwróci **PsApiManagementAccessInformation** , które modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3161b-119">Indicates that this cmdlet returns the **PsApiManagementAccessInformation** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="3161b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3161b-120">CommonParameters</span></span>
<span data-ttu-id="3161b-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3161b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3161b-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3161b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3161b-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3161b-123">INPUTS</span></span>

### <span data-ttu-id="3161b-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3161b-124">None</span></span>
<span data-ttu-id="3161b-125">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="3161b-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3161b-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3161b-126">OUTPUTS</span></span>

### <span data-ttu-id="3161b-127">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="3161b-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="3161b-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3161b-128">NOTES</span></span>

## <span data-ttu-id="3161b-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3161b-129">RELATED LINKS</span></span>

[<span data-ttu-id="3161b-130">Get-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="3161b-130">Get-AzureRmApiManagementTenantAccess</span></span>](./Get-AzureRmApiManagementTenantAccess.md)


