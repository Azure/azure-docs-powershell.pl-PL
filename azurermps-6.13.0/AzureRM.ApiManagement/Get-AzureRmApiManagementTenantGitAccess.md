---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementtenantgitaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantGitAccess.md
ms.openlocfilehash: 643877de4ab2b9107459beaa7acb276072a249ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543991"
---
# <span data-ttu-id="21a38-101">Get-AzureRmApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="21a38-101">Get-AzureRmApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="21a38-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="21a38-102">SYNOPSIS</span></span>
<span data-ttu-id="21a38-103">Pobiera konfigurację dostępu git dla dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="21a38-103">Gets the Git access configuration for a tenant.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21a38-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="21a38-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantGitAccess -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21a38-105">Opis</span><span class="sxs-lookup"><span data-stu-id="21a38-105">DESCRIPTION</span></span>
<span data-ttu-id="21a38-106">Polecenie cmdlet **Get-AzureRmApiManagementTenantGitAccess** Pobiera konfigurację dostępu git dla dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="21a38-106">The **Get-AzureRmApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="21a38-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="21a38-107">EXAMPLES</span></span>

### <span data-ttu-id="21a38-108">Przykład 1: Pobieranie konfiguracji dostępu dzierżawy</span><span class="sxs-lookup"><span data-stu-id="21a38-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementTenantGitAccess -Context $apimContext
```

<span data-ttu-id="21a38-109">To polecenie pobiera konfigurację dostępu git dla określonego kontekstu.</span><span class="sxs-lookup"><span data-stu-id="21a38-109">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="21a38-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="21a38-110">PARAMETERS</span></span>

### <span data-ttu-id="21a38-111">-Context</span><span class="sxs-lookup"><span data-stu-id="21a38-111">-Context</span></span>
<span data-ttu-id="21a38-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="21a38-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="21a38-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21a38-113">-DefaultProfile</span></span>
<span data-ttu-id="21a38-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="21a38-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21a38-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21a38-115">CommonParameters</span></span>
<span data-ttu-id="21a38-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21a38-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21a38-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21a38-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21a38-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21a38-118">INPUTS</span></span>

### <span data-ttu-id="21a38-119">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="21a38-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="21a38-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="21a38-120">OUTPUTS</span></span>

### <span data-ttu-id="21a38-121">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="21a38-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="21a38-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="21a38-122">NOTES</span></span>

## <span data-ttu-id="21a38-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="21a38-123">RELATED LINKS</span></span>
