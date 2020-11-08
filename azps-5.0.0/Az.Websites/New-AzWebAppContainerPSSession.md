---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappcontainerpssession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppContainerPSSession.md
ms.openlocfilehash: 2244eb06257d69005d64cc640d0ecd783bd30572
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232905"
---
# <span data-ttu-id="2ec6f-101">New-AzWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="2ec6f-101">New-AzWebAppContainerPSSession</span></span>

## <span data-ttu-id="2ec6f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2ec6f-102">SYNOPSIS</span></span>
<span data-ttu-id="2ec6f-103">New-AzWebAppContainerPSSession utworzy nową zdalną sesję programu PowerShell z kontenerem systemu Windows określonym w danej witrynie lub gnieździe i określoną grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="2ec6f-103">New-AzWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="2ec6f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2ec6f-104">SYNTAX</span></span>

### <span data-ttu-id="2ec6f-105">S1 (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="2ec6f-105">S1 (Default)</span></span>
```
New-AzWebAppContainerPSSession [[-SlotName] <String>] [-Force] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ec6f-106">S2</span><span class="sxs-lookup"><span data-stu-id="2ec6f-106">S2</span></span>
```
New-AzWebAppContainerPSSession [-Force] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ec6f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2ec6f-107">DESCRIPTION</span></span>
<span data-ttu-id="2ec6f-108">New-AzWebAppContainerPSSession utworzy nową zdalną sesję programu PowerShell z kontenerem systemu Windows określonym w danej witrynie lub gnieździe i określoną grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="2ec6f-108">New-AzWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="2ec6f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2ec6f-109">EXAMPLES</span></span>

### <span data-ttu-id="2ec6f-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2ec6f-110">Example 1</span></span>
```
PS C:\> $s = New-AzWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
PS C:\> Invoke-Command -Session $s -ScriptBlock{Get-Process}
```

<span data-ttu-id="2ec6f-111">Spowoduje to utworzenie nowej zdalnej sesji programu PowerShell w aplikacji kontenerowej systemu Windows ContosoASP i wyświetlenie procesów uruchomionych na kontenerze ContosoASP</span><span class="sxs-lookup"><span data-stu-id="2ec6f-111">This will create a new remote PowerShell Session into the windows container app ContosoASP and show the processes that are running on the container ContosoASP</span></span>

## <span data-ttu-id="2ec6f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2ec6f-112">PARAMETERS</span></span>

### <span data-ttu-id="2ec6f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ec6f-113">-DefaultProfile</span></span>
<span data-ttu-id="2ec6f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2ec6f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ec6f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2ec6f-115">-Force</span></span>
<span data-ttu-id="2ec6f-116">Tworzenie sesji programu PowerShell bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2ec6f-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="2ec6f-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2ec6f-117">-Name</span></span>
<span data-ttu-id="2ec6f-118">Nazwa aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="2ec6f-118">The name of the web app.</span></span>

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

### <span data-ttu-id="2ec6f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ec6f-119">-ResourceGroupName</span></span>
<span data-ttu-id="2ec6f-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2ec6f-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="2ec6f-121">-Slotname</span><span class="sxs-lookup"><span data-stu-id="2ec6f-121">-SlotName</span></span>
<span data-ttu-id="2ec6f-122">Nazwa miejsca aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="2ec6f-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="2ec6f-123">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="2ec6f-123">-WebApp</span></span>
<span data-ttu-id="2ec6f-124">Obiekt aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="2ec6f-124">The web app object</span></span>

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

### <span data-ttu-id="2ec6f-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2ec6f-125">-Confirm</span></span>
<span data-ttu-id="2ec6f-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ec6f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ec6f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ec6f-127">-WhatIf</span></span>
<span data-ttu-id="2ec6f-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ec6f-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2ec6f-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2ec6f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ec6f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ec6f-130">CommonParameters</span></span>
<span data-ttu-id="2ec6f-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ec6f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ec6f-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ec6f-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ec6f-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ec6f-133">INPUTS</span></span>

### <span data-ttu-id="2ec6f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2ec6f-134">System.String</span></span>

### <span data-ttu-id="2ec6f-135">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="2ec6f-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="2ec6f-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2ec6f-136">OUTPUTS</span></span>

### <span data-ttu-id="2ec6f-137">System. Management. Automation. Runspaces. PSSession</span><span class="sxs-lookup"><span data-stu-id="2ec6f-137">System.Management.Automation.Runspaces.PSSession</span></span>

## <span data-ttu-id="2ec6f-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2ec6f-138">NOTES</span></span>

## <span data-ttu-id="2ec6f-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2ec6f-139">RELATED LINKS</span></span>
