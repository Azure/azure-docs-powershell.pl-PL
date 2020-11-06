---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmRoleDefinition.md
ms.openlocfilehash: 2282bdef70f6352caa535b4d7a68d5e4046f831e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524937"
---
# <span data-ttu-id="20c95-101">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="20c95-101">Set-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="20c95-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="20c95-102">SYNOPSIS</span></span>
<span data-ttu-id="20c95-103">Modyfikuje rolę niestandardową w usłudze Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="20c95-103">Modifies a custom role in Azure RBAC.</span></span>
<span data-ttu-id="20c95-104">Podaj zmodyfikowaną definicję roli jako plik JSON lub jako PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="20c95-104">Provide the modified role definition either as a JSON file or as a PSRoleDefinition.</span></span>
<span data-ttu-id="20c95-105">Najpierw użyj polecenia Get-AzureRmRoleDefinition, aby pobrać rolę niestandardową, którą chcesz zmodyfikować.</span><span class="sxs-lookup"><span data-stu-id="20c95-105">First, use the Get-AzureRmRoleDefinition command to retrieve the custom role that you wish to modify.</span></span>
<span data-ttu-id="20c95-106">Następnie zmodyfikuj właściwości, które chcesz zmienić.</span><span class="sxs-lookup"><span data-stu-id="20c95-106">Then, modify the properties that you wish to change.</span></span>
<span data-ttu-id="20c95-107">Na koniec Zapisz definicję roli za pomocą tego polecenia.</span><span class="sxs-lookup"><span data-stu-id="20c95-107">Finally, save the role definition using this command.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20c95-108">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="20c95-108">SYNTAX</span></span>

### <span data-ttu-id="20c95-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="20c95-109">InputFileParameterSet</span></span>
```
Set-AzureRmRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20c95-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="20c95-110">RoleDefinitionParameterSet</span></span>
```
Set-AzureRmRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="20c95-111">Opis</span><span class="sxs-lookup"><span data-stu-id="20c95-111">DESCRIPTION</span></span>
<span data-ttu-id="20c95-112">Polecenie cmdlet Set-AzureRmRoleDefinition aktualizuje istniejącą rolę niestandardową w kontroli dostępu na platformie Azure Role-Based.</span><span class="sxs-lookup"><span data-stu-id="20c95-112">The Set-AzureRmRoleDefinition cmdlet updates an existing custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="20c95-113">Wprowadź zaktualizowaną definicję roli jako dane wejściowe polecenia jako plik JSON lub obiekt PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="20c95-113">Provide the updated role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="20c95-114">Definicja roli zaktualizowanej roli niestandardowej musi zawierać identyfikator i wszystkie inne wymagane właściwości roli, nawet jeśli nie zostały zaktualizowane: DisplayName, Description, Actions, AssignableScopes.</span><span class="sxs-lookup"><span data-stu-id="20c95-114">The role definition for the updated custom role MUST contain the Id and all other required properties of the role even if they are not updated: DisplayName, Description, Actions, AssignableScopes.</span></span>
<span data-ttu-id="20c95-115">Nienaruszone, akcje dataNotDataActions są opcjonalne.</span><span class="sxs-lookup"><span data-stu-id="20c95-115">NotActions, DataActions, NotDataActions are optional.</span></span>

<span data-ttu-id="20c95-116">Poniżej przedstawiono przykładowy kod JSON zaktualizowanej definicji ról dla Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="20c95-116">Following is a sample updated role definition json for Set-AzureRmRoleDefinition</span></span>

<span data-ttu-id="20c95-117">{"ID": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "nazwa": "uaktualniona rola", "opis": "może monitorować wszystkie zasoby i uruchamiać i ponownie uruchamiać maszyny wirtualne", "akcje": \[ " */Read", "Microsoft. ClassicCompute/virtualmachines/restart"; "Microsoft. ClassicCompute/virtualmachines/Start/Action" \] ; "zanaruszone": \[ "* /Write" \] ; "akcje danych": \[ "Microsoft. Storage/storageAccounts/blobServices/Containers/BLOB/Read", "NotDataActions": "Microsoft. Storage/storageAccounts/blobServices/Containers \] \[ /BLOB/Write", "AssignableScopes" \] : \[ "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" \] }</span><span class="sxs-lookup"><span data-stu-id="20c95-117">{ "Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ " */read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "* /write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="20c95-118">Przykłady</span><span class="sxs-lookup"><span data-stu-id="20c95-118">EXAMPLES</span></span>

### <span data-ttu-id="20c95-119">Aktualizowanie przy użyciu PSRoleDefinitionObject</span><span class="sxs-lookup"><span data-stu-id="20c95-119">Update using PSRoleDefinitionObject</span></span>
```
PS C:\> $roleDef = Get-AzureRmRoleDefinition "Contoso On-Call"
          PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
          PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
          PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")

          PS C:\> Set-AzureRmRoleDefinition -Role $roleDef
```

### <span data-ttu-id="20c95-120">Tworzenie przy użyciu pliku JSON</span><span class="sxs-lookup"><span data-stu-id="20c95-120">Create using JSON file</span></span>
```
PS C:\> Set-AzureRmRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="20c95-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="20c95-121">PARAMETERS</span></span>

### <span data-ttu-id="20c95-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20c95-122">-DefaultProfile</span></span>
<span data-ttu-id="20c95-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="20c95-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="20c95-124">-Plik_wejściowy</span><span class="sxs-lookup"><span data-stu-id="20c95-124">-InputFile</span></span>
<span data-ttu-id="20c95-125">Nazwa pliku zawierającego pojedynczą definicję roli JSON do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="20c95-125">File name containing a single json role definition to be updated.</span></span>
<span data-ttu-id="20c95-126">Uwzględnij tylko właściwości, które mają zostać zaktualizowane w notacji JSON.</span><span class="sxs-lookup"><span data-stu-id="20c95-126">Only include the properties that are to be updated in the JSON.</span></span>
<span data-ttu-id="20c95-127">Właściwość ID jest wymagana.</span><span class="sxs-lookup"><span data-stu-id="20c95-127">Id property is Required.</span></span>

```yaml
Type: String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20c95-128">-Rola</span><span class="sxs-lookup"><span data-stu-id="20c95-128">-Role</span></span>
<span data-ttu-id="20c95-129">Obiekt definicji roli do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="20c95-129">Role definition object to be updated</span></span>

```yaml
Type: PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20c95-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20c95-130">CommonParameters</span></span>
<span data-ttu-id="20c95-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20c95-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20c95-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20c95-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20c95-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="20c95-133">INPUTS</span></span>

### <span data-ttu-id="20c95-134">PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="20c95-134">PSRoleDefinition</span></span>
<span data-ttu-id="20c95-135">Parametr "rola" akceptuje wartość typu "PSRoleDefinition" z procesu</span><span class="sxs-lookup"><span data-stu-id="20c95-135">Parameter 'Role' accepts value of type 'PSRoleDefinition' from the pipeline</span></span>

## <span data-ttu-id="20c95-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="20c95-136">OUTPUTS</span></span>

### <span data-ttu-id="20c95-137">Microsoft. Azure. Commands. resources. models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="20c95-137">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="20c95-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="20c95-138">NOTES</span></span>
<span data-ttu-id="20c95-139">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="20c95-139">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="20c95-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="20c95-140">RELATED LINKS</span></span>

[<span data-ttu-id="20c95-141">Get-AzureRmProviderOperation</span><span class="sxs-lookup"><span data-stu-id="20c95-141">Get-AzureRmProviderOperation</span></span>](./Get-AzureRmProviderOperation.md)

[<span data-ttu-id="20c95-142">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="20c95-142">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="20c95-143">Nowe — AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="20c95-143">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="20c95-144">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="20c95-144">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)

