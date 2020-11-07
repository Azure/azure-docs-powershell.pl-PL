---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantAccess.md
ms.openlocfilehash: 30243ef1796e621d0898aae38e29ddb1dc7fd20b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552471"
---
# <span data-ttu-id="4d18e-101">Get-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="4d18e-101">Get-AzureRmApiManagementTenantAccess</span></span>

## <span data-ttu-id="4d18e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4d18e-102">SYNOPSIS</span></span>
<span data-ttu-id="4d18e-103">Pobiera konfigurację dostępu dla dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="4d18e-103">Gets the access configuration for a tenant.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d18e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4d18e-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantAccess -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d18e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4d18e-105">DESCRIPTION</span></span>
<span data-ttu-id="4d18e-106">Polecenie cmdlet **Get-AzureRmApiManagementTenantAccess** Pobiera konfigurację dostępu dzierżawy dla dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="4d18e-106">The **Get-AzureRmApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>

## <span data-ttu-id="4d18e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4d18e-107">EXAMPLES</span></span>

### <span data-ttu-id="4d18e-108">Przykład 1: Pobieranie konfiguracji dostępu dzierżawy</span><span class="sxs-lookup"><span data-stu-id="4d18e-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>Get-AzureRmApiManagementTenantAccess -Context $ApimContext
```

<span data-ttu-id="4d18e-109">To polecenie pobiera konfigurację dostępu dzierżawy dla określonego kontekstu.</span><span class="sxs-lookup"><span data-stu-id="4d18e-109">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="4d18e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4d18e-110">PARAMETERS</span></span>

### <span data-ttu-id="4d18e-111">-Context</span><span class="sxs-lookup"><span data-stu-id="4d18e-111">-Context</span></span>
<span data-ttu-id="4d18e-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="4d18e-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="4d18e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d18e-113">-DefaultProfile</span></span>
<span data-ttu-id="4d18e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4d18e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d18e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d18e-115">CommonParameters</span></span>
<span data-ttu-id="4d18e-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d18e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d18e-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d18e-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d18e-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d18e-118">INPUTS</span></span>

## <span data-ttu-id="4d18e-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4d18e-119">OUTPUTS</span></span>

### <span data-ttu-id="4d18e-120">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="4d18e-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="4d18e-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4d18e-121">NOTES</span></span>

## <span data-ttu-id="4d18e-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4d18e-122">RELATED LINKS</span></span>

[<span data-ttu-id="4d18e-123">Set-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="4d18e-123">Set-AzureRmApiManagementTenantAccess</span></span>](./Set-AzureRmApiManagementTenantAccess.md)

