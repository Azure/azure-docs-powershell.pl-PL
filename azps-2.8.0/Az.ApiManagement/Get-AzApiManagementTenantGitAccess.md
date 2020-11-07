---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
ms.openlocfilehash: 3338ae75406cc7c9253b21a52726f283f19d4ad7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707052"
---
# <span data-ttu-id="b9917-101">Get-AzApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="b9917-101">Get-AzApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="b9917-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b9917-102">SYNOPSIS</span></span>
<span data-ttu-id="b9917-103">Pobiera konfigurację dostępu git dla dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="b9917-103">Gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="b9917-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b9917-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b9917-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b9917-105">DESCRIPTION</span></span>
<span data-ttu-id="b9917-106">Polecenie cmdlet **Get-AzApiManagementTenantGitAccess** Pobiera konfigurację dostępu git dla dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="b9917-106">The **Get-AzApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="b9917-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b9917-107">EXAMPLES</span></span>

### <span data-ttu-id="b9917-108">Przykład 1: Pobieranie konfiguracji dostępu dzierżawy</span><span class="sxs-lookup"><span data-stu-id="b9917-108">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccess -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="b9917-109">To polecenie pobiera konfigurację dostępu git dla określonego kontekstu.</span><span class="sxs-lookup"><span data-stu-id="b9917-109">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="b9917-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b9917-110">PARAMETERS</span></span>

### <span data-ttu-id="b9917-111">-Context</span><span class="sxs-lookup"><span data-stu-id="b9917-111">-Context</span></span>
<span data-ttu-id="b9917-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="b9917-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b9917-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9917-113">-DefaultProfile</span></span>
<span data-ttu-id="b9917-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b9917-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9917-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9917-115">CommonParameters</span></span>
<span data-ttu-id="b9917-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9917-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9917-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9917-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9917-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b9917-118">INPUTS</span></span>

### <span data-ttu-id="b9917-119">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b9917-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="b9917-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b9917-120">OUTPUTS</span></span>

### <span data-ttu-id="b9917-121">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="b9917-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="b9917-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b9917-122">NOTES</span></span>

## <span data-ttu-id="b9917-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b9917-123">RELATED LINKS</span></span>