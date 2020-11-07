---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappcontainerpssession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppContainerPSSession.md
ms.openlocfilehash: 651ca91a8da5a025040127b4e3bbcedf16225faf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871420"
---
# <span data-ttu-id="12ee2-101">New-AzWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="12ee2-101">New-AzWebAppContainerPSSession</span></span>

## <span data-ttu-id="12ee2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="12ee2-102">SYNOPSIS</span></span>
<span data-ttu-id="12ee2-103">New-AzWebAppContainerPSSession utworzy nową zdalną sesję programu PowerShell z kontenerem systemu Windows określonym w danej witrynie lub gnieździe i określoną grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="12ee2-103">New-AzWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="12ee2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="12ee2-104">SYNTAX</span></span>

### <span data-ttu-id="12ee2-105">S1 (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="12ee2-105">S1 (Default)</span></span>
```
New-AzWebAppContainerPSSession [[-SlotName] <String>] [-Force] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12ee2-106">S2</span><span class="sxs-lookup"><span data-stu-id="12ee2-106">S2</span></span>
```
New-AzWebAppContainerPSSession [-Force] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12ee2-107">Opis</span><span class="sxs-lookup"><span data-stu-id="12ee2-107">DESCRIPTION</span></span>
<span data-ttu-id="12ee2-108">New-AzWebAppContainerPSSession utworzy nową zdalną sesję programu PowerShell z kontenerem systemu Windows określonym w danej witrynie lub gnieździe i określoną grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="12ee2-108">New-AzWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="12ee2-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="12ee2-109">EXAMPLES</span></span>

### <span data-ttu-id="12ee2-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="12ee2-110">Example 1</span></span>
```
PS C:\> $s = New-AzWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
PS C:\> Invoke-Command -Session $s -ScriptBlock{Get-Process}
```

<span data-ttu-id="12ee2-111">Spowoduje to utworzenie nowej zdalnej sesji programu PowerShell w aplikacji kontenerowej systemu Windows ContosoASP i wyświetlenie procesów uruchomionych na kontenerze ContosoASP</span><span class="sxs-lookup"><span data-stu-id="12ee2-111">This will create a new remote PowerShell Session into the windows container app ContosoASP and show the processes that are running on the container ContosoASP</span></span>

## <span data-ttu-id="12ee2-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="12ee2-112">PARAMETERS</span></span>

### <span data-ttu-id="12ee2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12ee2-113">-DefaultProfile</span></span>
<span data-ttu-id="12ee2-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="12ee2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12ee2-115">-Force</span><span class="sxs-lookup"><span data-stu-id="12ee2-115">-Force</span></span>
<span data-ttu-id="12ee2-116">Tworzenie sesji programu PowerShell bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="12ee2-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="12ee2-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="12ee2-117">-Name</span></span>
<span data-ttu-id="12ee2-118">Nazwa aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="12ee2-118">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12ee2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12ee2-119">-ResourceGroupName</span></span>
<span data-ttu-id="12ee2-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="12ee2-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12ee2-121">-Slotname</span><span class="sxs-lookup"><span data-stu-id="12ee2-121">-SlotName</span></span>
<span data-ttu-id="12ee2-122">Nazwa miejsca aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="12ee2-122">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12ee2-123">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="12ee2-123">-WebApp</span></span>
<span data-ttu-id="12ee2-124">Obiekt aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="12ee2-124">The web app object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12ee2-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="12ee2-125">-Confirm</span></span>
<span data-ttu-id="12ee2-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12ee2-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12ee2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12ee2-127">-WhatIf</span></span>
<span data-ttu-id="12ee2-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12ee2-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="12ee2-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="12ee2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12ee2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12ee2-130">CommonParameters</span></span>
<span data-ttu-id="12ee2-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12ee2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12ee2-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12ee2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12ee2-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="12ee2-133">INPUTS</span></span>

### <span data-ttu-id="12ee2-134">System. String</span><span class="sxs-lookup"><span data-stu-id="12ee2-134">System.String</span></span>

### <span data-ttu-id="12ee2-135">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="12ee2-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="12ee2-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="12ee2-136">OUTPUTS</span></span>

### <span data-ttu-id="12ee2-137">System. Management. Automation. Runspaces. PSSession</span><span class="sxs-lookup"><span data-stu-id="12ee2-137">System.Management.Automation.Runspaces.PSSession</span></span>

## <span data-ttu-id="12ee2-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="12ee2-138">NOTES</span></span>

## <span data-ttu-id="12ee2-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="12ee2-139">RELATED LINKS</span></span>
