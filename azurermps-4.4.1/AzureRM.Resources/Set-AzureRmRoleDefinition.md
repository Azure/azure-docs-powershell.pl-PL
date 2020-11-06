---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmRoleDefinition.md
ms.openlocfilehash: 9f5927905e492fd93998e12f97a97a0380755905
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546080"
---
# <span data-ttu-id="f460f-101">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f460f-101">Set-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="f460f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f460f-102">SYNOPSIS</span></span>
<span data-ttu-id="f460f-103">Modyfikuje rolę niestandardową w usłudze Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="f460f-103">Modifies a custom role in Azure RBAC.</span></span>
<span data-ttu-id="f460f-104">Podaj zmodyfikowaną definicję roli jako plik JSON lub jako PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="f460f-104">Provide the modified role definition either as a JSON file or as a PSRoleDefinition.</span></span>
<span data-ttu-id="f460f-105">Najpierw użyj polecenia Get-AzureRmRoleDefinition, aby pobrać rolę niestandardową, którą chcesz zmodyfikować.</span><span class="sxs-lookup"><span data-stu-id="f460f-105">First, use the Get-AzureRmRoleDefinition command to retrieve the custom role that you wish to modify.</span></span>
<span data-ttu-id="f460f-106">Następnie zmodyfikuj właściwości, które chcesz zmienić.</span><span class="sxs-lookup"><span data-stu-id="f460f-106">Then, modify the properties that you wish to change.</span></span>
<span data-ttu-id="f460f-107">Na koniec Zapisz definicję roli za pomocą tego polecenia.</span><span class="sxs-lookup"><span data-stu-id="f460f-107">Finally, save the role definition using this command.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f460f-108">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f460f-108">SYNTAX</span></span>

### <span data-ttu-id="f460f-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="f460f-109">InputFileParameterSet</span></span>
```
Set-AzureRmRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f460f-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="f460f-110">RoleDefinitionParameterSet</span></span>
```
Set-AzureRmRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f460f-111">Opis</span><span class="sxs-lookup"><span data-stu-id="f460f-111">DESCRIPTION</span></span>
<span data-ttu-id="f460f-112">Polecenie cmdlet Set-AzureRmRoleDefinition aktualizuje istniejącą rolę niestandardową w kontroli dostępu na platformie Azure Role-Based.</span><span class="sxs-lookup"><span data-stu-id="f460f-112">The Set-AzureRmRoleDefinition cmdlet updates an existing custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="f460f-113">Wprowadź zaktualizowaną definicję roli jako dane wejściowe polecenia jako plik JSON lub obiekt PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="f460f-113">Provide the updated role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="f460f-114">Definicja roli zaktualizowanej roli niestandardowej musi zawierać identyfikator i wszystkie inne wymagane właściwości roli, nawet jeśli nie zostały zaktualizowane: DisplayName, Description, Actions, AssignableScopes.</span><span class="sxs-lookup"><span data-stu-id="f460f-114">The role definition for the updated custom role MUST contain the Id and all other required properties of the role even if they are not updated: DisplayName, Description, Actions, AssignableScopes.</span></span>
<span data-ttu-id="f460f-115">Nienaruszone są opcjonalne.</span><span class="sxs-lookup"><span data-stu-id="f460f-115">NotActions is optional.</span></span>

<span data-ttu-id="f460f-116">Poniżej przedstawiono przykładowy kod JSON zaktualizowanej definicji ról dla Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f460f-116">Following is a sample updated role definition json for Set-AzureRmRoleDefinition</span></span>

<span data-ttu-id="f460f-117">{"ID": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "nazwa": "uaktualniona rola", "opis": "może monitorować wszystkie zasoby i uruchamiać i ponownie uruchamiać maszyny wirtualne", "akcje": \[ "\*/read", "Microsoft. ClassicCompute/virtualmachines/restart/Action", "Microsoft. ClassicCompute/virtualmachines/Start/Action" \] "AssignableScopes": \[ "/subscriptions/4004a9fd-d58e-48DC-aeb2-4a4aec58606f" \] }</span><span class="sxs-lookup"><span data-stu-id="f460f-117">{ "Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ "\*/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \] "AssignableScopes": \["/subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f"\] }</span></span>

## <span data-ttu-id="f460f-118">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f460f-118">EXAMPLES</span></span>

### <span data-ttu-id="f460f-119">Aktualizacja--------------------------przy użyciu--------------------------PSRoleDefinitionObject</span><span class="sxs-lookup"><span data-stu-id="f460f-119">--------------------------  Update using PSRoleDefinitionObject  --------------------------</span></span>
```
PS C:\> $roleDef = Get-AzureRmRoleDefinition "Contoso On-Call"
          PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
          PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
          PS C:\> $roleDef.AssignableScopes = @("/subscriptions/eb910d4f-edbf-429b-94F6-d76bae7ff401", "/subscriptions/a846d197-5eac-45c7-b885-a6227fe6d388")

          PS C:\> New-AzureRmRoleDefinition -Role $roleDef
```

### <span data-ttu-id="f460f-120">--------------------------Utworzyć przy użyciu pliku JSON--------------------------</span><span class="sxs-lookup"><span data-stu-id="f460f-120">--------------------------  Create using JSON file  --------------------------</span></span>
```
PS C:\> Set-AzureRmRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="f460f-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f460f-121">PARAMETERS</span></span>

### <span data-ttu-id="f460f-122">-Plik_wejściowy</span><span class="sxs-lookup"><span data-stu-id="f460f-122">-InputFile</span></span>
<span data-ttu-id="f460f-123">Nazwa pliku zawierającego pojedynczą definicję roli JSON do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="f460f-123">File name containing a single json role definition to be updated.</span></span>
<span data-ttu-id="f460f-124">Uwzględnij tylko właściwości, które mają zostać zaktualizowane w notacji JSON.</span><span class="sxs-lookup"><span data-stu-id="f460f-124">Only include the properties that are to be updated in the JSON.</span></span>
<span data-ttu-id="f460f-125">Właściwość ID jest wymagana.</span><span class="sxs-lookup"><span data-stu-id="f460f-125">Id property is Required.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f460f-126">-Rola</span><span class="sxs-lookup"><span data-stu-id="f460f-126">-Role</span></span>
<span data-ttu-id="f460f-127">Obiekt definicji roli do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="f460f-127">Role definition object to be updated</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f460f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f460f-128">-DefaultProfile</span></span>
<span data-ttu-id="f460f-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f460f-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f460f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f460f-130">CommonParameters</span></span>
<span data-ttu-id="f460f-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f460f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f460f-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f460f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f460f-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f460f-133">INPUTS</span></span>

### <span data-ttu-id="f460f-134">PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f460f-134">PSRoleDefinition</span></span>
<span data-ttu-id="f460f-135">Parametr "rola" akceptuje wartość typu "PSRoleDefinition" z procesu</span><span class="sxs-lookup"><span data-stu-id="f460f-135">Parameter 'Role' accepts value of type 'PSRoleDefinition' from the pipeline</span></span>

## <span data-ttu-id="f460f-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f460f-136">OUTPUTS</span></span>

### <span data-ttu-id="f460f-137">Microsoft. Azure. Commands. resources. models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f460f-137">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="f460f-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f460f-138">NOTES</span></span>
<span data-ttu-id="f460f-139">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="f460f-139">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="f460f-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f460f-140">RELATED LINKS</span></span>

[<span data-ttu-id="f460f-141">Get-AzureRmProviderOperation</span><span class="sxs-lookup"><span data-stu-id="f460f-141">Get-AzureRmProviderOperation</span></span>](./Get-AzureRmProviderOperation.md)

[<span data-ttu-id="f460f-142">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f460f-142">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="f460f-143">Nowe — AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f460f-143">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="f460f-144">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f460f-144">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)

