---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6221C40F-63FC-4D66-B6BD-01024AFF3B65
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Save-AzureRmApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Save-AzureRmApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 91cd7855b832a406fdd3ce9a959135936ee3c284
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552451"
---
# <span data-ttu-id="bc5c3-101">Save-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="bc5c3-101">Save-AzureRmApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="bc5c3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bc5c3-102">SYNOPSIS</span></span>
<span data-ttu-id="bc5c3-103">Zapisuje zmiany, tworząc zatwierdzenie bieżącej konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="bc5c3-103">Saves changes by creating a commit for current configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc5c3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bc5c3-104">SYNTAX</span></span>

```
Save-AzureRmApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc5c3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bc5c3-105">DESCRIPTION</span></span>
<span data-ttu-id="bc5c3-106">Polecenie cmdlet **Save-AzureRmApiManagementTenantGitConfiguration** zapisuje zmiany, tworząc przekazanie zawierające bieżącą migawkę konfiguracji do gałęzi w repozytorium.</span><span class="sxs-lookup"><span data-stu-id="bc5c3-106">The **Save-AzureRmApiManagementTenantGitConfiguration** cmdlet saves the changes by creating a commit that contains the current configuration snapshot to a branch in the repository.</span></span>

## <span data-ttu-id="bc5c3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bc5c3-107">EXAMPLES</span></span>

### <span data-ttu-id="bc5c3-108">Przykład 1. Zapisz zmiany w konfiguracji</span><span class="sxs-lookup"><span data-stu-id="bc5c3-108">Example 1: Save changes to configuration</span></span>
```
PS C:\>Save-AzureRmApiManagementTenantGitConfiguration -Context $ApimContext -Branch 'master' -PassThru
```

<span data-ttu-id="bc5c3-109">To polecenie zapisuje zmiany przez utworzenie zatwierdzenia z bieżącą migawką konfiguracji do określonej gałęzi w repozytorium.</span><span class="sxs-lookup"><span data-stu-id="bc5c3-109">This command saves the changes by creating a commit with the current configuration snapshot to the specified branch in the repository.</span></span>

## <span data-ttu-id="bc5c3-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bc5c3-110">PARAMETERS</span></span>

### <span data-ttu-id="bc5c3-111">-Branch</span><span class="sxs-lookup"><span data-stu-id="bc5c3-111">-Branch</span></span>
<span data-ttu-id="bc5c3-112">Określa nazwę gałęzi git, w której należy przekazać bieżącą migawkę konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="bc5c3-112">Specifies the name of the Git branch in which to commit the current configuration snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc5c3-113">-Context</span><span class="sxs-lookup"><span data-stu-id="bc5c3-113">-Context</span></span>
<span data-ttu-id="bc5c3-114">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="bc5c3-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="bc5c3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="bc5c3-115">-Force</span></span>
<span data-ttu-id="bc5c3-116">Określa, że to polecenie cmdlet przekazuje bieżącą bazę danych konfiguracji do repozytorium git, nawet jeśli repozytorium git zawiera nowsze zmiany, które zostały zastąpione.</span><span class="sxs-lookup"><span data-stu-id="bc5c3-116">Specifies that this cmdlet commits the current configuration database to the Git repository, even if the Git repository has newer changes that are overwritten.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc5c3-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bc5c3-117">-PassThru</span></span>
<span data-ttu-id="bc5c3-118">Wskazuje, że to polecenie cmdlet zwraca obiekt **PsApiManagementOperationResult** .</span><span class="sxs-lookup"><span data-stu-id="bc5c3-118">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc5c3-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bc5c3-119">-Confirm</span></span>
<span data-ttu-id="bc5c3-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc5c3-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc5c3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc5c3-121">-WhatIf</span></span>
<span data-ttu-id="bc5c3-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc5c3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc5c3-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bc5c3-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc5c3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc5c3-124">-DefaultProfile</span></span>
<span data-ttu-id="bc5c3-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bc5c3-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc5c3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc5c3-126">CommonParameters</span></span>
<span data-ttu-id="bc5c3-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc5c3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc5c3-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc5c3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc5c3-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc5c3-129">INPUTS</span></span>

## <span data-ttu-id="bc5c3-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bc5c3-130">OUTPUTS</span></span>

### <span data-ttu-id="bc5c3-131">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="bc5c3-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="bc5c3-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bc5c3-132">NOTES</span></span>

## <span data-ttu-id="bc5c3-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bc5c3-133">RELATED LINKS</span></span>

[<span data-ttu-id="bc5c3-134">Publikowanie — AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="bc5c3-134">Publish-AzureRmApiManagementTenantGitConfiguration</span></span>](./Publish-AzureRmApiManagementTenantGitConfiguration.md)


