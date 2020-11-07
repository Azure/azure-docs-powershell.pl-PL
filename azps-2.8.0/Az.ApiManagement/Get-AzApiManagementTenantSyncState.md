---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 288EF15B-FE5C-44AE-ABD5-2B92F408B9EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantsyncstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
ms.openlocfilehash: c8d3ff0d268c4a84269585af7e769b46af663f5c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707051"
---
# <span data-ttu-id="aa3fd-101">Get-AzApiManagementTenantSyncState</span><span class="sxs-lookup"><span data-stu-id="aa3fd-101">Get-AzApiManagementTenantSyncState</span></span>

## <span data-ttu-id="aa3fd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aa3fd-102">SYNOPSIS</span></span>
<span data-ttu-id="aa3fd-103">Pobiera stan ostatniej synchronizacji bazy danych konfiguracji i repozytorium git.</span><span class="sxs-lookup"><span data-stu-id="aa3fd-103">Gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="aa3fd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aa3fd-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantSyncState -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aa3fd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="aa3fd-105">DESCRIPTION</span></span>
<span data-ttu-id="aa3fd-106">Polecenie cmdlet **Get-AzApiManagementTenantSyncState** Pobiera stan ostatniej synchronizacji bazy danych konfiguracji i repozytorium git.</span><span class="sxs-lookup"><span data-stu-id="aa3fd-106">The **Get-AzApiManagementTenantSyncState** cmdlet gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="aa3fd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aa3fd-107">EXAMPLES</span></span>

### <span data-ttu-id="aa3fd-108">Przykład 1: uzyskiwanie stanu ostatniej synchronizacji</span><span class="sxs-lookup"><span data-stu-id="aa3fd-108">Example 1: Get the status of the most recent synchronization</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantSyncState -Context $apimContext
```

<span data-ttu-id="aa3fd-109">To polecenie uzyskuje stan ostatniej synchronizacji między bazą danych konfiguracji a repozytorium git.</span><span class="sxs-lookup"><span data-stu-id="aa3fd-109">This command gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="aa3fd-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aa3fd-110">PARAMETERS</span></span>

### <span data-ttu-id="aa3fd-111">-Context</span><span class="sxs-lookup"><span data-stu-id="aa3fd-111">-Context</span></span>
<span data-ttu-id="aa3fd-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="aa3fd-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="aa3fd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa3fd-113">-DefaultProfile</span></span>
<span data-ttu-id="aa3fd-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="aa3fd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa3fd-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa3fd-115">CommonParameters</span></span>
<span data-ttu-id="aa3fd-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa3fd-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa3fd-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa3fd-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa3fd-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa3fd-118">INPUTS</span></span>

### <span data-ttu-id="aa3fd-119">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="aa3fd-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="aa3fd-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aa3fd-120">OUTPUTS</span></span>

### <span data-ttu-id="aa3fd-121">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementTenantConfigurationSyncState</span><span class="sxs-lookup"><span data-stu-id="aa3fd-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementTenantConfigurationSyncState</span></span>

## <span data-ttu-id="aa3fd-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aa3fd-122">NOTES</span></span>

## <span data-ttu-id="aa3fd-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aa3fd-123">RELATED LINKS</span></span>