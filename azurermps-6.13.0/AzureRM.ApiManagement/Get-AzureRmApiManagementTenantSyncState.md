---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 288EF15B-FE5C-44AE-ABD5-2B92F408B9EB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementtenantsyncstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantSyncState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantSyncState.md
ms.openlocfilehash: c75660c60788d5b2a099be97c927328464f34dba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542071"
---
# <span data-ttu-id="fe5b0-101">Get-AzureRmApiManagementTenantSyncState</span><span class="sxs-lookup"><span data-stu-id="fe5b0-101">Get-AzureRmApiManagementTenantSyncState</span></span>

## <span data-ttu-id="fe5b0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fe5b0-102">SYNOPSIS</span></span>
<span data-ttu-id="fe5b0-103">Pobiera stan ostatniej synchronizacji bazy danych konfiguracji i repozytorium git.</span><span class="sxs-lookup"><span data-stu-id="fe5b0-103">Gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe5b0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fe5b0-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantSyncState -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe5b0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fe5b0-105">DESCRIPTION</span></span>
<span data-ttu-id="fe5b0-106">Polecenie cmdlet **Get-AzureRmApiManagementTenantSyncState** Pobiera stan ostatniej synchronizacji bazy danych konfiguracji i repozytorium git.</span><span class="sxs-lookup"><span data-stu-id="fe5b0-106">The **Get-AzureRmApiManagementTenantSyncState** cmdlet gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="fe5b0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fe5b0-107">EXAMPLES</span></span>

### <span data-ttu-id="fe5b0-108">Przykład 1: uzyskiwanie stanu ostatniej synchronizacji</span><span class="sxs-lookup"><span data-stu-id="fe5b0-108">Example 1: Get the status of the most recent synchronization</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementTenantSyncState -Context $apimContext
```

<span data-ttu-id="fe5b0-109">To polecenie uzyskuje stan ostatniej synchronizacji między bazą danych konfiguracji a repozytorium git.</span><span class="sxs-lookup"><span data-stu-id="fe5b0-109">This command gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="fe5b0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fe5b0-110">PARAMETERS</span></span>

### <span data-ttu-id="fe5b0-111">-Context</span><span class="sxs-lookup"><span data-stu-id="fe5b0-111">-Context</span></span>
<span data-ttu-id="fe5b0-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="fe5b0-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="fe5b0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe5b0-113">-DefaultProfile</span></span>
<span data-ttu-id="fe5b0-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fe5b0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe5b0-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe5b0-115">CommonParameters</span></span>
<span data-ttu-id="fe5b0-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe5b0-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe5b0-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe5b0-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe5b0-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe5b0-118">INPUTS</span></span>

### <span data-ttu-id="fe5b0-119">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="fe5b0-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="fe5b0-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fe5b0-120">OUTPUTS</span></span>

### <span data-ttu-id="fe5b0-121">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementTenantConfigurationSyncState</span><span class="sxs-lookup"><span data-stu-id="fe5b0-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementTenantConfigurationSyncState</span></span>

## <span data-ttu-id="fe5b0-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fe5b0-122">NOTES</span></span>

## <span data-ttu-id="fe5b0-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fe5b0-123">RELATED LINKS</span></span>
