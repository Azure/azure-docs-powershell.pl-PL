---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplication.md
ms.openlocfilehash: c2604531014283b3599adb94c4a12d70761e1533
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304758"
---
# <span data-ttu-id="a78d7-101">Remove-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="a78d7-101">Remove-AzWvdApplication</span></span>

## <span data-ttu-id="a78d7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a78d7-102">SYNOPSIS</span></span>
<span data-ttu-id="a78d7-103">Usuwanie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a78d7-103">Remove an application.</span></span>

## <span data-ttu-id="a78d7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a78d7-104">SYNTAX</span></span>

### <span data-ttu-id="a78d7-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="a78d7-105">Delete (Default)</span></span>
```
Remove-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a78d7-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a78d7-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a78d7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a78d7-107">DESCRIPTION</span></span>
<span data-ttu-id="a78d7-108">Usuwanie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a78d7-108">Remove an application.</span></span>

## <span data-ttu-id="a78d7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a78d7-109">EXAMPLES</span></span>

### <span data-ttu-id="a78d7-110">Przykład 1: Usuwanie aplikacji pulpitu wirtualnego systemu Windows według nazwy</span><span class="sxs-lookup"><span data-stu-id="a78d7-110">Example 1: Delete a Windows Virtual Desktop Application by name</span></span>
```powershell
PS C:\> Remove-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name ApplicationName
```

<span data-ttu-id="a78d7-111">To polecenie usuwa aplikację klasyczną Windows Virtual w grupie Applicaton.</span><span class="sxs-lookup"><span data-stu-id="a78d7-111">This command deletes a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="a78d7-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a78d7-112">PARAMETERS</span></span>

### <span data-ttu-id="a78d7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a78d7-113">-DefaultProfile</span></span>
<span data-ttu-id="a78d7-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a78d7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a78d7-115">-GroupName</span><span class="sxs-lookup"><span data-stu-id="a78d7-115">-GroupName</span></span>
<span data-ttu-id="a78d7-116">Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="a78d7-116">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a78d7-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a78d7-117">-InputObject</span></span>
<span data-ttu-id="a78d7-118">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="a78d7-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a78d7-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a78d7-119">-Name</span></span>
<span data-ttu-id="a78d7-120">Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="a78d7-120">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a78d7-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a78d7-121">-PassThru</span></span>
<span data-ttu-id="a78d7-122">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="a78d7-122">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a78d7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a78d7-123">-ResourceGroupName</span></span>
<span data-ttu-id="a78d7-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a78d7-124">The name of the resource group.</span></span>
<span data-ttu-id="a78d7-125">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="a78d7-125">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a78d7-126">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a78d7-126">-SubscriptionId</span></span>
<span data-ttu-id="a78d7-127">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="a78d7-127">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a78d7-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a78d7-128">-Confirm</span></span>
<span data-ttu-id="a78d7-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a78d7-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a78d7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a78d7-130">-WhatIf</span></span>
<span data-ttu-id="a78d7-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a78d7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a78d7-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a78d7-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a78d7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a78d7-133">CommonParameters</span></span>
<span data-ttu-id="a78d7-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a78d7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a78d7-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a78d7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a78d7-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a78d7-136">INPUTS</span></span>

### <span data-ttu-id="a78d7-137">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="a78d7-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="a78d7-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a78d7-138">OUTPUTS</span></span>

### <span data-ttu-id="a78d7-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a78d7-139">System.Boolean</span></span>

## <span data-ttu-id="a78d7-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a78d7-140">NOTES</span></span>

<span data-ttu-id="a78d7-141">PISUJE</span><span class="sxs-lookup"><span data-stu-id="a78d7-141">ALIASES</span></span>

<span data-ttu-id="a78d7-142">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a78d7-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a78d7-143">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="a78d7-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a78d7-144">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a78d7-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a78d7-145">INPUTobject <IDesktopVirtualizationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="a78d7-145">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a78d7-146">`[ApplicationGroupName <String>]`: Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="a78d7-146">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="a78d7-147">`[ApplicationName <String>]`: Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="a78d7-147">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="a78d7-148">`[DesktopName <String>]`: Nazwa pulpitu w określonej grupie pulpit</span><span class="sxs-lookup"><span data-stu-id="a78d7-148">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="a78d7-149">`[HostPoolName <String>]`: Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="a78d7-149">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="a78d7-150">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="a78d7-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a78d7-151">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a78d7-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a78d7-152">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="a78d7-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="a78d7-153">`[SessionHostName <String>]`: Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="a78d7-153">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="a78d7-154">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="a78d7-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a78d7-155">`[UserSessionId <String>]`: Nazwa sesji użytkownika w określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="a78d7-155">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="a78d7-156">`[WorkspaceName <String>]`: Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="a78d7-156">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="a78d7-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a78d7-157">RELATED LINKS</span></span>

