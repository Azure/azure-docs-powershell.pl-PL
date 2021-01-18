---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccesssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
ms.openlocfilehash: 51aea46ea65081dd63a3f9f9de4a3a80f4ae8986
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502458"
---
# <span data-ttu-id="e234c-101">Get-AzApiManagementTenantGitAccessSecret</span><span class="sxs-lookup"><span data-stu-id="e234c-101">Get-AzApiManagementTenantGitAccessSecret</span></span>

## <span data-ttu-id="e234c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e234c-102">SYNOPSIS</span></span>
<span data-ttu-id="e234c-103">Pobiera klucze konfiguracji dostępu git dla dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="e234c-103">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="e234c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e234c-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccessSecret -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e234c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e234c-105">DESCRIPTION</span></span>
<span data-ttu-id="e234c-106">Pobiera klucze konfiguracji dostępu git dla dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="e234c-106">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="e234c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e234c-107">EXAMPLES</span></span>

### <span data-ttu-id="e234c-108">Przykład 1: Pobieranie konfiguracji dostępu dzierżawy</span><span class="sxs-lookup"><span data-stu-id="e234c-108">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccessSecret -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="e234c-109">To polecenie pobiera klucze konfiguracji dostępu git dla określonego kontekstu.</span><span class="sxs-lookup"><span data-stu-id="e234c-109">This command gets the Git access configuration keys for the specified context.</span></span>

## <span data-ttu-id="e234c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e234c-110">PARAMETERS</span></span>

### <span data-ttu-id="e234c-111">-Context</span><span class="sxs-lookup"><span data-stu-id="e234c-111">-Context</span></span>
<span data-ttu-id="e234c-112">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="e234c-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e234c-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="e234c-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e234c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e234c-114">-DefaultProfile</span></span>
<span data-ttu-id="e234c-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e234c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e234c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e234c-116">CommonParameters</span></span>
<span data-ttu-id="e234c-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e234c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e234c-118">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e234c-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e234c-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e234c-119">INPUTS</span></span>

### <span data-ttu-id="e234c-120">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e234c-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="e234c-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e234c-121">OUTPUTS</span></span>

### <span data-ttu-id="e234c-122">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="e234c-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="e234c-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e234c-123">NOTES</span></span>

## <span data-ttu-id="e234c-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e234c-124">RELATED LINKS</span></span>
