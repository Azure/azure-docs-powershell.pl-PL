---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantAccess.md
ms.openlocfilehash: 64f341398ff20f3eddf67c88c51a93125904d566
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544600"
---
# <span data-ttu-id="7d71e-101">Get-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="7d71e-101">Get-AzureRmApiManagementTenantAccess</span></span>

## <span data-ttu-id="7d71e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7d71e-102">SYNOPSIS</span></span>
<span data-ttu-id="7d71e-103">Pobiera konfigurację dostępu dla dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="7d71e-103">Gets the access configuration for a tenant.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d71e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7d71e-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantAccess -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d71e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7d71e-105">DESCRIPTION</span></span>
<span data-ttu-id="7d71e-106">Polecenie cmdlet **Get-AzureRmApiManagementTenantAccess** Pobiera konfigurację dostępu dzierżawy dla dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="7d71e-106">The **Get-AzureRmApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>

## <span data-ttu-id="7d71e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7d71e-107">EXAMPLES</span></span>

### <span data-ttu-id="7d71e-108">Przykład 1: Pobieranie konfiguracji dostępu dzierżawy</span><span class="sxs-lookup"><span data-stu-id="7d71e-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementTenantAccess -Context $apimContext 
```

<span data-ttu-id="7d71e-109">To polecenie pobiera konfigurację dostępu dzierżawy dla określonego kontekstu.</span><span class="sxs-lookup"><span data-stu-id="7d71e-109">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="7d71e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7d71e-110">PARAMETERS</span></span>

### <span data-ttu-id="7d71e-111">-Context</span><span class="sxs-lookup"><span data-stu-id="7d71e-111">-Context</span></span>
<span data-ttu-id="7d71e-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="7d71e-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="7d71e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d71e-113">-DefaultProfile</span></span>
<span data-ttu-id="7d71e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7d71e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="7d71e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d71e-115">CommonParameters</span></span>
<span data-ttu-id="7d71e-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d71e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d71e-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d71e-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d71e-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7d71e-118">INPUTS</span></span>

### <span data-ttu-id="7d71e-119">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7d71e-119">None</span></span>
<span data-ttu-id="7d71e-120">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="7d71e-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7d71e-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7d71e-121">OUTPUTS</span></span>

### <span data-ttu-id="7d71e-122">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="7d71e-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="7d71e-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7d71e-123">NOTES</span></span>

## <span data-ttu-id="7d71e-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7d71e-124">RELATED LINKS</span></span>

[<span data-ttu-id="7d71e-125">Set-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="7d71e-125">Set-AzureRmApiManagementTenantAccess</span></span>](./Set-AzureRmApiManagementTenantAccess.md)


