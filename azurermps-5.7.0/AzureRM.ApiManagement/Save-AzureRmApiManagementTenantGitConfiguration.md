---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 6221C40F-63FC-4D66-B6BD-01024AFF3B65
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/save-azurermapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Save-AzureRmApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Save-AzureRmApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 7401c359a9af82d1b65749a3276aada89ab9320d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525382"
---
# <span data-ttu-id="4f421-101">Save-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="4f421-101">Save-AzureRmApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="4f421-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4f421-102">SYNOPSIS</span></span>
<span data-ttu-id="4f421-103">Zapisuje zmiany, tworząc zatwierdzenie bieżącej konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="4f421-103">Saves changes by creating a commit for current configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f421-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4f421-104">SYNTAX</span></span>

```
Save-AzureRmApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f421-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4f421-105">DESCRIPTION</span></span>
<span data-ttu-id="4f421-106">Polecenie cmdlet **Save-AzureRmApiManagementTenantGitConfiguration** zapisuje zmiany, tworząc przekazanie zawierające bieżącą migawkę konfiguracji do gałęzi w repozytorium.</span><span class="sxs-lookup"><span data-stu-id="4f421-106">The **Save-AzureRmApiManagementTenantGitConfiguration** cmdlet saves the changes by creating a commit that contains the current configuration snapshot to a branch in the repository.</span></span>

## <span data-ttu-id="4f421-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4f421-107">EXAMPLES</span></span>

### <span data-ttu-id="4f421-108">Przykład 1. Zapisz zmiany w konfiguracji</span><span class="sxs-lookup"><span data-stu-id="4f421-108">Example 1: Save changes to configuration</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Save-AzureRmApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="4f421-109">To polecenie zapisuje zmiany przez utworzenie zatwierdzenia z bieżącą migawką konfiguracji do określonej gałęzi w repozytorium.</span><span class="sxs-lookup"><span data-stu-id="4f421-109">This command saves the changes by creating a commit with the current configuration snapshot to the specified branch in the repository.</span></span>

## <span data-ttu-id="4f421-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4f421-110">PARAMETERS</span></span>

### <span data-ttu-id="4f421-111">-Branch</span><span class="sxs-lookup"><span data-stu-id="4f421-111">-Branch</span></span>
<span data-ttu-id="4f421-112">Określa nazwę gałęzi git, w której należy przekazać bieżącą migawkę konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="4f421-112">Specifies the name of the Git branch in which to commit the current configuration snapshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f421-113">-Context</span><span class="sxs-lookup"><span data-stu-id="4f421-113">-Context</span></span>
<span data-ttu-id="4f421-114">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="4f421-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="4f421-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f421-115">-DefaultProfile</span></span>
<span data-ttu-id="4f421-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4f421-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="4f421-117">-Force</span><span class="sxs-lookup"><span data-stu-id="4f421-117">-Force</span></span>
<span data-ttu-id="4f421-118">Określa, że to polecenie cmdlet przekazuje bieżącą bazę danych konfiguracji do repozytorium git, nawet jeśli repozytorium git zawiera nowsze zmiany, które zostały zastąpione.</span><span class="sxs-lookup"><span data-stu-id="4f421-118">Specifies that this cmdlet commits the current configuration database to the Git repository, even if the Git repository has newer changes that are overwritten.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f421-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f421-119">-PassThru</span></span>
<span data-ttu-id="4f421-120">Wskazuje, że to polecenie cmdlet zwraca obiekt **PsApiManagementOperationResult** .</span><span class="sxs-lookup"><span data-stu-id="4f421-120">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f421-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4f421-121">-Confirm</span></span>
<span data-ttu-id="4f421-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f421-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f421-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f421-123">-WhatIf</span></span>
<span data-ttu-id="4f421-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f421-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f421-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4f421-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f421-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f421-126">CommonParameters</span></span>
<span data-ttu-id="4f421-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f421-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f421-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f421-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f421-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4f421-129">INPUTS</span></span>

### <span data-ttu-id="4f421-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4f421-130">None</span></span>
<span data-ttu-id="4f421-131">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="4f421-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4f421-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4f421-132">OUTPUTS</span></span>

### <span data-ttu-id="4f421-133">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="4f421-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="4f421-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4f421-134">NOTES</span></span>

## <span data-ttu-id="4f421-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4f421-135">RELATED LINKS</span></span>

[<span data-ttu-id="4f421-136">Publikowanie — AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="4f421-136">Publish-AzureRmApiManagementTenantGitConfiguration</span></span>](./Publish-AzureRmApiManagementTenantGitConfiguration.md)


