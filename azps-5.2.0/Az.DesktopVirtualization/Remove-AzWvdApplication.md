---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplication.md
ms.openlocfilehash: c65fd55599a78bbaa558ba7ec8efa94fdc3b40e2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338461"
---
# <span data-ttu-id="8450b-101">Remove-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="8450b-101">Remove-AzWvdApplication</span></span>

## <span data-ttu-id="8450b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8450b-102">SYNOPSIS</span></span>
<span data-ttu-id="8450b-103">Usuwanie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8450b-103">Remove an application.</span></span>

## <span data-ttu-id="8450b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8450b-104">SYNTAX</span></span>

### <span data-ttu-id="8450b-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="8450b-105">Delete (Default)</span></span>
```
Remove-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8450b-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8450b-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8450b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8450b-107">DESCRIPTION</span></span>
<span data-ttu-id="8450b-108">Usuwanie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8450b-108">Remove an application.</span></span>

## <span data-ttu-id="8450b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8450b-109">EXAMPLES</span></span>

### <span data-ttu-id="8450b-110">Przykład 1: Usuwanie aplikacji pulpitu wirtualnego systemu Windows według nazwy</span><span class="sxs-lookup"><span data-stu-id="8450b-110">Example 1: Delete a Windows Virtual Desktop Application by name</span></span>
```powershell
PS C:\> Remove-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name ApplicationName
```

<span data-ttu-id="8450b-111">To polecenie usuwa aplikację klasyczną Windows Virtual w grupie Applicaton.</span><span class="sxs-lookup"><span data-stu-id="8450b-111">This command deletes a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="8450b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8450b-112">PARAMETERS</span></span>

### <span data-ttu-id="8450b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8450b-113">-DefaultProfile</span></span>
<span data-ttu-id="8450b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8450b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8450b-115">-GroupName</span><span class="sxs-lookup"><span data-stu-id="8450b-115">-GroupName</span></span>
<span data-ttu-id="8450b-116">Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="8450b-116">The name of the application group</span></span>

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

### <span data-ttu-id="8450b-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8450b-117">-InputObject</span></span>
<span data-ttu-id="8450b-118">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="8450b-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8450b-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8450b-119">-Name</span></span>
<span data-ttu-id="8450b-120">Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="8450b-120">The name of the application within the specified application group</span></span>

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

### <span data-ttu-id="8450b-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8450b-121">-PassThru</span></span>
<span data-ttu-id="8450b-122">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="8450b-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8450b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8450b-123">-ResourceGroupName</span></span>
<span data-ttu-id="8450b-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8450b-124">The name of the resource group.</span></span>
<span data-ttu-id="8450b-125">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="8450b-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="8450b-126">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="8450b-126">-SubscriptionId</span></span>
<span data-ttu-id="8450b-127">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="8450b-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="8450b-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8450b-128">-Confirm</span></span>
<span data-ttu-id="8450b-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8450b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8450b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8450b-130">-WhatIf</span></span>
<span data-ttu-id="8450b-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8450b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8450b-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8450b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8450b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8450b-133">CommonParameters</span></span>
<span data-ttu-id="8450b-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8450b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8450b-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8450b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8450b-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8450b-136">INPUTS</span></span>

### <span data-ttu-id="8450b-137">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="8450b-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="8450b-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8450b-138">OUTPUTS</span></span>

### <span data-ttu-id="8450b-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8450b-139">System.Boolean</span></span>

## <span data-ttu-id="8450b-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8450b-140">NOTES</span></span>

<span data-ttu-id="8450b-141">PISUJE</span><span class="sxs-lookup"><span data-stu-id="8450b-141">ALIASES</span></span>

<span data-ttu-id="8450b-142">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8450b-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8450b-143">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="8450b-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8450b-144">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8450b-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8450b-145">INPUTobject <IDesktopVirtualizationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="8450b-145">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8450b-146">`[ApplicationGroupName <String>]`: Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="8450b-146">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="8450b-147">`[ApplicationName <String>]`: Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="8450b-147">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="8450b-148">`[DesktopName <String>]`: Nazwa pulpitu w określonej grupie pulpit</span><span class="sxs-lookup"><span data-stu-id="8450b-148">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="8450b-149">`[HostPoolName <String>]`: Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="8450b-149">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="8450b-150">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="8450b-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8450b-151">`[MsixPackageFullName <String>]`: Pakiet specyficzny dla wersji pełna nazwa pakietu MSIX w określonym hostpool</span><span class="sxs-lookup"><span data-stu-id="8450b-151">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="8450b-152">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8450b-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8450b-153">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="8450b-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="8450b-154">`[SessionHostName <String>]`: Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="8450b-154">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="8450b-155">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="8450b-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="8450b-156">`[UserSessionId <String>]`: Nazwa sesji użytkownika w określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="8450b-156">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="8450b-157">`[WorkspaceName <String>]`: Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="8450b-157">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="8450b-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8450b-158">RELATED LINKS</span></span>

