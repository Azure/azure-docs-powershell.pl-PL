---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 4783305F-5619-446A-A6DF-BD1E56739A2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/publish-azurermapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Publish-AzureRmApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Publish-AzureRmApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 3879def437171e9de2cad6f328ef6bf15bed3d48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544568"
---
# <span data-ttu-id="9506a-101">Publish-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="9506a-101">Publish-AzureRmApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="9506a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9506a-102">SYNOPSIS</span></span>
<span data-ttu-id="9506a-103">Publikuje zmiany z gałęzi Git w bazie danych konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="9506a-103">Publishes changes from a Git branch to the configuration database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9506a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9506a-104">SYNTAX</span></span>

```
Publish-AzureRmApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-ValidateOnly] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9506a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9506a-105">DESCRIPTION</span></span>
<span data-ttu-id="9506a-106">Polecenie cmdlet **Publish-AzureRmApiManagementTenantGitConfiguration** publikuje zmiany z gałęzi Git w bazie danych konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="9506a-106">The **Publish-AzureRmApiManagementTenantGitConfiguration** cmdlet publishes the changes from a Git branch to the configuration database.</span></span>
<span data-ttu-id="9506a-107">Możesz również sprawdzić poprawność zmian w gałęzi git bez publikowania.</span><span class="sxs-lookup"><span data-stu-id="9506a-107">You can alternatively validate the changes in a Git branch without publishing.</span></span>

## <span data-ttu-id="9506a-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9506a-108">EXAMPLES</span></span>

### <span data-ttu-id="9506a-109">Przykład 1: wdrażanie zmian git</span><span class="sxs-lookup"><span data-stu-id="9506a-109">Example 1: Deploy Git changes</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzureRmApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="9506a-110">To polecenie umożliwia publikowanie zmian z określonej gałęzi do bazy danych konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="9506a-110">This command publishes the changes from the specified branch to the configuration database.</span></span>

### <span data-ttu-id="9506a-111">Przykład 2: sprawdzanie poprawności zmian git</span><span class="sxs-lookup"><span data-stu-id="9506a-111">Example 2: Validate Git changes</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzureRmApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -ValidateOnly -PassThru
```

<span data-ttu-id="9506a-112">To polecenie sprawdza poprawność zmian w gałęzi usługi git dla bazy danych konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="9506a-112">This command validates the changes in the Git branch against the configuration database.</span></span>
<span data-ttu-id="9506a-113">Zmiany nie są publikowane.</span><span class="sxs-lookup"><span data-stu-id="9506a-113">It does not publish changes.</span></span>

## <span data-ttu-id="9506a-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9506a-114">PARAMETERS</span></span>

### <span data-ttu-id="9506a-115">-Branch</span><span class="sxs-lookup"><span data-stu-id="9506a-115">-Branch</span></span>
<span data-ttu-id="9506a-116">Określa nazwę gałęzi git, z której to polecenie cmdlet wdraża konfigurację w bazie danych konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="9506a-116">Specifies the name of the Git branch from which this cmdlet deploys the configuration to the configuration database.</span></span>

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

### <span data-ttu-id="9506a-117">-Context</span><span class="sxs-lookup"><span data-stu-id="9506a-117">-Context</span></span>
<span data-ttu-id="9506a-118">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="9506a-118">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="9506a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9506a-119">-DefaultProfile</span></span>
<span data-ttu-id="9506a-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9506a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="9506a-121">-Force</span><span class="sxs-lookup"><span data-stu-id="9506a-121">-Force</span></span>
<span data-ttu-id="9506a-122">Wskazuje, że to polecenie cmdlet usunie subskrypcje produktów, które zostały usunięte w tej aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="9506a-122">Indicates that this cmdlet deletes subscriptions to products that are deleted in this update.</span></span>

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

### <span data-ttu-id="9506a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9506a-123">-PassThru</span></span>
<span data-ttu-id="9506a-124">Wskazuje, że to polecenie cmdlet zwraca obiekt **PsApiManagementOperationResult** .</span><span class="sxs-lookup"><span data-stu-id="9506a-124">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="9506a-125">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="9506a-125">-ValidateOnly</span></span>
<span data-ttu-id="9506a-126">Wskazuje, że to polecenie cmdlet sprawdza poprawność zmian w określonej gałęzi git.</span><span class="sxs-lookup"><span data-stu-id="9506a-126">Indicates that this cmdlet validates the changes in the specified Git branch.</span></span>
<span data-ttu-id="9506a-127">Nie jest on publikowany w bazie danych konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="9506a-127">It does not publish to the configuration database.</span></span>

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

### <span data-ttu-id="9506a-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9506a-128">-Confirm</span></span>
<span data-ttu-id="9506a-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9506a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9506a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9506a-130">-WhatIf</span></span>
<span data-ttu-id="9506a-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9506a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9506a-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9506a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9506a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9506a-133">CommonParameters</span></span>
<span data-ttu-id="9506a-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9506a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9506a-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9506a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9506a-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9506a-136">INPUTS</span></span>

### <span data-ttu-id="9506a-137">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9506a-137">None</span></span>
<span data-ttu-id="9506a-138">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="9506a-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9506a-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9506a-139">OUTPUTS</span></span>

### <span data-ttu-id="9506a-140">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="9506a-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="9506a-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9506a-141">NOTES</span></span>

## <span data-ttu-id="9506a-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9506a-142">RELATED LINKS</span></span>

[<span data-ttu-id="9506a-143">Zapisz — AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="9506a-143">Save-AzureRmApiManagementTenantGitConfiguration</span></span>](./Save-AzureRmApiManagementTenantGitConfiguration.md)


