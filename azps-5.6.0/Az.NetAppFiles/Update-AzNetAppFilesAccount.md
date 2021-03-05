---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/update-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
ms.openlocfilehash: 2a31b5af374b1bc0f6136da61aa1c3672274e913
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968145"
---
# <span data-ttu-id="f2084-101">Update-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="f2084-101">Update-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="f2084-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2084-102">SYNOPSIS</span></span>
<span data-ttu-id="f2084-103">Aktualizuje konto usługi Azure NetApp Files (ANF) zgodnie z dostępnymi opcjonalnymi modyfikatorami.</span><span class="sxs-lookup"><span data-stu-id="f2084-103">Updates an Azure NetApp Files (ANF) account according to the optional modifiers provided.</span></span>

## <span data-ttu-id="f2084-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f2084-104">SYNTAX</span></span>

### <span data-ttu-id="f2084-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="f2084-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2084-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2084-106">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 -ResourceId <String> [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2084-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2084-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] -InputObject <PSNetAppFilesAccount> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2084-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="f2084-108">DESCRIPTION</span></span>
<span data-ttu-id="f2084-109">Polecenie **cmdlet Update-AzNetAppFilesAccount** modyfikuje konto ANF.</span><span class="sxs-lookup"><span data-stu-id="f2084-109">The **Update-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="f2084-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f2084-110">EXAMPLES</span></span>

### <span data-ttu-id="f2084-111">Przykład 1. Aktualizacja konta ANF</span><span class="sxs-lookup"><span data-stu-id="f2084-111">Example 1 : Updates an ANF account</span></span>
```
PS C:\>Update-AzNetAppFilesAccount -ResourceGroupName "MyRG" -l "westus2" -Name "MyAnfAccount" -Tag @{'Tag1' = 'Value1'}

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              : {Tag1}
AccountId         : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
ActiveDirectories :
ProvisioningState : Succeeded
```

<span data-ttu-id="f2084-112">To polecenie wykonuje aktualizację na danym koncie, modyfikując tagi do podanych.</span><span class="sxs-lookup"><span data-stu-id="f2084-112">This command performs an update on the given account modifying the tags to those provided.</span></span>

## <span data-ttu-id="f2084-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2084-113">PARAMETERS</span></span>

### <span data-ttu-id="f2084-114">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="f2084-114">-ActiveDirectory</span></span>
<span data-ttu-id="f2084-115">Tablica z hasztagami reprezentująca aktywne katalogi</span><span class="sxs-lookup"><span data-stu-id="f2084-115">A hashtable array which represents the active directories</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2084-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2084-116">-DefaultProfile</span></span>
<span data-ttu-id="f2084-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f2084-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2084-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2084-118">-InputObject</span></span>
<span data-ttu-id="f2084-119">Obiekt konta do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="f2084-119">The account object to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2084-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f2084-120">-Location</span></span>
<span data-ttu-id="f2084-121">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="f2084-121">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2084-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f2084-122">-Name</span></span>
<span data-ttu-id="f2084-123">Nazwa konta ANF</span><span class="sxs-lookup"><span data-stu-id="f2084-123">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2084-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2084-124">-ResourceGroupName</span></span>
<span data-ttu-id="f2084-125">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="f2084-125">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2084-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2084-126">-ResourceId</span></span>
<span data-ttu-id="f2084-127">Identyfikator zasobu konta ANF</span><span class="sxs-lookup"><span data-stu-id="f2084-127">The resource id of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2084-128">— Tag</span><span class="sxs-lookup"><span data-stu-id="f2084-128">-Tag</span></span>
<span data-ttu-id="f2084-129">Tabela skrótów reprezentująca tagi zasobów</span><span class="sxs-lookup"><span data-stu-id="f2084-129">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2084-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f2084-130">-Confirm</span></span>
<span data-ttu-id="f2084-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f2084-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2084-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2084-132">-WhatIf</span></span>
<span data-ttu-id="f2084-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2084-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2084-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f2084-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2084-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2084-135">CommonParameters</span></span>
<span data-ttu-id="f2084-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2084-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2084-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2084-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2084-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2084-138">INPUTS</span></span>

### <span data-ttu-id="f2084-139">System.String</span><span class="sxs-lookup"><span data-stu-id="f2084-139">System.String</span></span>

### <span data-ttu-id="f2084-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="f2084-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="f2084-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2084-141">OUTPUTS</span></span>

### <span data-ttu-id="f2084-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="f2084-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="f2084-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f2084-143">NOTES</span></span>

## <span data-ttu-id="f2084-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f2084-144">RELATED LINKS</span></span>
