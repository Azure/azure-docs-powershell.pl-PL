---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementtenantgitaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantGitAccess.md
ms.openlocfilehash: 28b27ee7a2e24b425d5ffa93be4d1f3513a31c08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544592"
---
# <span data-ttu-id="8d220-101">Get-AzureRmApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="8d220-101">Get-AzureRmApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="8d220-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8d220-102">SYNOPSIS</span></span>
<span data-ttu-id="8d220-103">Pobiera konfigurację dostępu git dla dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="8d220-103">Gets the Git access configuration for a tenant.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d220-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8d220-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantGitAccess -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d220-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8d220-105">DESCRIPTION</span></span>
<span data-ttu-id="8d220-106">Polecenie cmdlet **Get-AzureRmApiManagementTenantGitAccess** Pobiera konfigurację dostępu git dla dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="8d220-106">The **Get-AzureRmApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="8d220-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8d220-107">EXAMPLES</span></span>

### <span data-ttu-id="8d220-108">Przykład 1: Pobieranie konfiguracji dostępu dzierżawy</span><span class="sxs-lookup"><span data-stu-id="8d220-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementTenantGitAccess -Context $apimContext 
```

<span data-ttu-id="8d220-109">To polecenie pobiera konfigurację dostępu git dla określonego kontekstu.</span><span class="sxs-lookup"><span data-stu-id="8d220-109">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="8d220-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8d220-110">PARAMETERS</span></span>

### <span data-ttu-id="8d220-111">-Context</span><span class="sxs-lookup"><span data-stu-id="8d220-111">-Context</span></span>
<span data-ttu-id="8d220-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="8d220-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="8d220-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d220-113">-DefaultProfile</span></span>
<span data-ttu-id="8d220-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8d220-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="8d220-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d220-115">CommonParameters</span></span>
<span data-ttu-id="8d220-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d220-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d220-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d220-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d220-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8d220-118">INPUTS</span></span>

### <span data-ttu-id="8d220-119">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="8d220-119">None</span></span>
<span data-ttu-id="8d220-120">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="8d220-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8d220-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8d220-121">OUTPUTS</span></span>

### <span data-ttu-id="8d220-122">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="8d220-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="8d220-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8d220-123">NOTES</span></span>

## <span data-ttu-id="8d220-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8d220-124">RELATED LINKS</span></span>

