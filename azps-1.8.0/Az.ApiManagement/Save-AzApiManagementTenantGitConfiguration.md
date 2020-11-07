---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6221C40F-63FC-4D66-B6BD-01024AFF3B65
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/save-azapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Save-AzApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Save-AzApiManagementTenantGitConfiguration.md
ms.openlocfilehash: b4abd2d8dab9e4c41d2e42be77bee62428ccc712
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869380"
---
# <span data-ttu-id="5e62e-101">Save-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="5e62e-101">Save-AzApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="5e62e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5e62e-102">SYNOPSIS</span></span>
<span data-ttu-id="5e62e-103">Zapisuje zmiany, tworząc zatwierdzenie bieżącej konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="5e62e-103">Saves changes by creating a commit for current configuration.</span></span>

## <span data-ttu-id="5e62e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5e62e-104">SYNTAX</span></span>

```
Save-AzApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e62e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5e62e-105">DESCRIPTION</span></span>
<span data-ttu-id="5e62e-106">Polecenie cmdlet **Save-AzApiManagementTenantGitConfiguration** zapisuje zmiany, tworząc przekazanie zawierające bieżącą migawkę konfiguracji do gałęzi w repozytorium.</span><span class="sxs-lookup"><span data-stu-id="5e62e-106">The **Save-AzApiManagementTenantGitConfiguration** cmdlet saves the changes by creating a commit that contains the current configuration snapshot to a branch in the repository.</span></span>

## <span data-ttu-id="5e62e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5e62e-107">EXAMPLES</span></span>

### <span data-ttu-id="5e62e-108">Przykład 1. Zapisz zmiany w konfiguracji</span><span class="sxs-lookup"><span data-stu-id="5e62e-108">Example 1: Save changes to configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Save-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="5e62e-109">To polecenie zapisuje zmiany przez utworzenie zatwierdzenia z bieżącą migawką konfiguracji do określonej gałęzi w repozytorium.</span><span class="sxs-lookup"><span data-stu-id="5e62e-109">This command saves the changes by creating a commit with the current configuration snapshot to the specified branch in the repository.</span></span>

## <span data-ttu-id="5e62e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5e62e-110">PARAMETERS</span></span>

### <span data-ttu-id="5e62e-111">-Branch</span><span class="sxs-lookup"><span data-stu-id="5e62e-111">-Branch</span></span>
<span data-ttu-id="5e62e-112">Określa nazwę gałęzi git, w której należy przekazać bieżącą migawkę konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="5e62e-112">Specifies the name of the Git branch in which to commit the current configuration snapshot.</span></span>

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

### <span data-ttu-id="5e62e-113">-Context</span><span class="sxs-lookup"><span data-stu-id="5e62e-113">-Context</span></span>
<span data-ttu-id="5e62e-114">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="5e62e-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="5e62e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e62e-115">-DefaultProfile</span></span>
<span data-ttu-id="5e62e-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5e62e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e62e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="5e62e-117">-Force</span></span>
<span data-ttu-id="5e62e-118">Określa, że to polecenie cmdlet przekazuje bieżącą bazę danych konfiguracji do repozytorium git, nawet jeśli repozytorium git zawiera nowsze zmiany, które zostały zastąpione.</span><span class="sxs-lookup"><span data-stu-id="5e62e-118">Specifies that this cmdlet commits the current configuration database to the Git repository, even if the Git repository has newer changes that are overwritten.</span></span>

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

### <span data-ttu-id="5e62e-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e62e-119">-PassThru</span></span>
<span data-ttu-id="5e62e-120">Wskazuje, że to polecenie cmdlet zwraca obiekt **PsApiManagementOperationResult** .</span><span class="sxs-lookup"><span data-stu-id="5e62e-120">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="5e62e-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5e62e-121">-Confirm</span></span>
<span data-ttu-id="5e62e-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e62e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e62e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e62e-123">-WhatIf</span></span>
<span data-ttu-id="5e62e-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e62e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e62e-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5e62e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e62e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e62e-126">CommonParameters</span></span>
<span data-ttu-id="5e62e-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e62e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e62e-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e62e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e62e-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5e62e-129">INPUTS</span></span>

### <span data-ttu-id="5e62e-130">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5e62e-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5e62e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="5e62e-131">System.String</span></span>

### <span data-ttu-id="5e62e-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5e62e-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5e62e-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5e62e-133">OUTPUTS</span></span>

### <span data-ttu-id="5e62e-134">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="5e62e-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="5e62e-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5e62e-135">NOTES</span></span>

## <span data-ttu-id="5e62e-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5e62e-136">RELATED LINKS</span></span>

[<span data-ttu-id="5e62e-137">Publikowanie — AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="5e62e-137">Publish-AzApiManagementTenantGitConfiguration</span></span>](./Publish-AzApiManagementTenantGitConfiguration.md)


