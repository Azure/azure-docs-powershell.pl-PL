---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/?view=azurermps-6.8.1
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppContainerPSSession.md
ms.openlocfilehash: 3c5efcd51a8b546acb5fa9b8ed3623c40ddfb1e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525886"
---
# <span data-ttu-id="b2898-101">New-AzureRmWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="b2898-101">New-AzureRmWebAppContainerPSSession</span></span>

## <span data-ttu-id="b2898-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b2898-102">SYNOPSIS</span></span>
<span data-ttu-id="b2898-103">New-AzureRmWebAppContainerPSSession utworzy nową zdalną sesję programu PowerShell z kontenerem systemu Windows określonym w danej witrynie lub gnieździe i określoną grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="b2898-103">New-AzureRmWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2898-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b2898-104">SYNTAX</span></span>

### <span data-ttu-id="b2898-105">S1 (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="b2898-105">S1 (Default)</span></span>
```
New-AzureRmWebAppContainerPSSession [[-SlotName] <String>] [-Force] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2898-106">S2</span><span class="sxs-lookup"><span data-stu-id="b2898-106">S2</span></span>
```
New-AzureRmWebAppContainerPSSession [-Force] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2898-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b2898-107">DESCRIPTION</span></span>
<span data-ttu-id="b2898-108">New-AzureRmWebAppContainerPSSession utworzy nową zdalną sesję programu PowerShell z kontenerem systemu Windows określonym w danej witrynie lub gnieździe i określoną grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="b2898-108">New-AzureRmWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="b2898-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b2898-109">EXAMPLES</span></span>

### <span data-ttu-id="b2898-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b2898-110">Example 1</span></span>
```
PS C:\> $s = New-AzureRmWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
PS C:\> Invoke-Command -Session $s -ScriptBlock{Get-Process}
```

<span data-ttu-id="b2898-111">Spowoduje to utworzenie nowej zdalnej sesji programu PowerShell w aplikacji kontenerowej systemu Windows ContosoASP i wyświetlenie procesów uruchomionych na kontenerze ContosoASP</span><span class="sxs-lookup"><span data-stu-id="b2898-111">This will create a new remote PowerShell Session into the windows container app ContosoASP and show the processes that are running on the container ContosoASP</span></span>

## <span data-ttu-id="b2898-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b2898-112">PARAMETERS</span></span>

### <span data-ttu-id="b2898-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2898-113">-DefaultProfile</span></span>
<span data-ttu-id="b2898-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b2898-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2898-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b2898-115">-Force</span></span>
<span data-ttu-id="b2898-116">Tworzenie sesji programu PowerShell bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b2898-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="b2898-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b2898-117">-Name</span></span>
<span data-ttu-id="b2898-118">Nazwa aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="b2898-118">The name of the web app.</span></span>

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

### <span data-ttu-id="b2898-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2898-119">-ResourceGroupName</span></span>
<span data-ttu-id="b2898-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b2898-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="b2898-121">-Slotname</span><span class="sxs-lookup"><span data-stu-id="b2898-121">-SlotName</span></span>
<span data-ttu-id="b2898-122">Nazwa miejsca aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="b2898-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="b2898-123">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="b2898-123">-WebApp</span></span>
<span data-ttu-id="b2898-124">Obiekt aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="b2898-124">The web app object</span></span>

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

### <span data-ttu-id="b2898-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b2898-125">-Confirm</span></span>
<span data-ttu-id="b2898-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2898-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2898-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2898-127">-WhatIf</span></span>
<span data-ttu-id="b2898-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2898-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b2898-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b2898-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2898-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2898-130">CommonParameters</span></span>
<span data-ttu-id="b2898-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2898-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2898-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2898-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2898-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b2898-133">INPUTS</span></span>

### <span data-ttu-id="b2898-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b2898-134">System.String</span></span>
### <span data-ttu-id="b2898-135">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="b2898-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>
## <span data-ttu-id="b2898-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b2898-136">OUTPUTS</span></span>

### <span data-ttu-id="b2898-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b2898-137">System.String</span></span>
## <span data-ttu-id="b2898-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b2898-138">NOTES</span></span>

## <span data-ttu-id="b2898-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b2898-139">RELATED LINKS</span></span>
