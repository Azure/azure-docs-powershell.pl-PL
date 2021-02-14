---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/set-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
ms.openlocfilehash: ecbf6a847ad208b49e11ab0089f9cf486763ddf3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190010"
---
# <span data-ttu-id="500fa-101">Set-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="500fa-101">Set-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="500fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="500fa-102">SYNOPSIS</span></span>
<span data-ttu-id="500fa-103">Aktualizuje konto usługi Azure NetApp Files (ANF) przy użyciu nowego zestawu danych.</span><span class="sxs-lookup"><span data-stu-id="500fa-103">Updates an Azure NetApp Files (ANF) account with the new data set.</span></span> <span data-ttu-id="500fa-104">Przydatne w przypadku usuwania skojarzonych aktywnych katalogów.</span><span class="sxs-lookup"><span data-stu-id="500fa-104">Useful for deletion of associated active directories.</span></span>

## <span data-ttu-id="500fa-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="500fa-105">SYNTAX</span></span>

### <span data-ttu-id="500fa-106">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="500fa-106">ByFieldsParameterSet (Default)</span></span>
```
Set-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="500fa-107">SetByResourceActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="500fa-107">SetByResourceActiveDirectory</span></span>
```
Set-AzNetAppFilesAccount -Location <String> -Name <String> [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="500fa-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="500fa-108">DESCRIPTION</span></span>
<span data-ttu-id="500fa-109">Polecenie **cmdlet Set-AzNetAppFilesAccount** modyfikuje konto ANF.</span><span class="sxs-lookup"><span data-stu-id="500fa-109">The **Set-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="500fa-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="500fa-110">EXAMPLES</span></span>

### <span data-ttu-id="500fa-111">Przykład 1. Modyfikowanie konta ANF</span><span class="sxs-lookup"><span data-stu-id="500fa-111">Example 1 : Modify an ANF account</span></span>
```
PS C:\>Set-AzNetAppFilesAccount -ResourceGroupName "MyRG" -l "westus2" -Name "MyAnfAccount"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
AccountId         : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
ActiveDirectories : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="500fa-112">To polecenie wykonuje aktualizację dla danego konta.</span><span class="sxs-lookup"><span data-stu-id="500fa-112">This command performs an update on the given account.</span></span> <span data-ttu-id="500fa-113">Brak usługi Active Directory oznacza, że zostanie ona usunięta z konta.</span><span class="sxs-lookup"><span data-stu-id="500fa-113">The absence of the active directory means it will be removed from the account.</span></span>

## <span data-ttu-id="500fa-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="500fa-114">PARAMETERS</span></span>

### <span data-ttu-id="500fa-115">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="500fa-115">-ActiveDirectory</span></span>
<span data-ttu-id="500fa-116">Tablica z hasztagami reprezentująca aktywne katalogi</span><span class="sxs-lookup"><span data-stu-id="500fa-116">A hashtable array which represents the active directories</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory[]
Parameter Sets: SetByResourceActiveDirectory
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="500fa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="500fa-117">-DefaultProfile</span></span>
<span data-ttu-id="500fa-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="500fa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="500fa-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="500fa-119">-Location</span></span>
<span data-ttu-id="500fa-120">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="500fa-120">The location of the resource</span></span>

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

### <span data-ttu-id="500fa-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="500fa-121">-Name</span></span>
<span data-ttu-id="500fa-122">Nazwa konta ANF</span><span class="sxs-lookup"><span data-stu-id="500fa-122">The name of the ANF account</span></span>

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

### <span data-ttu-id="500fa-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="500fa-123">-ResourceGroupName</span></span>
<span data-ttu-id="500fa-124">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="500fa-124">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="500fa-125">— Tag</span><span class="sxs-lookup"><span data-stu-id="500fa-125">-Tag</span></span>
<span data-ttu-id="500fa-126">Tabela skrótów reprezentująca tagi zasobów</span><span class="sxs-lookup"><span data-stu-id="500fa-126">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="500fa-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="500fa-127">-Confirm</span></span>
<span data-ttu-id="500fa-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="500fa-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="500fa-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="500fa-129">-WhatIf</span></span>
<span data-ttu-id="500fa-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="500fa-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="500fa-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="500fa-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="500fa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="500fa-132">CommonParameters</span></span>
<span data-ttu-id="500fa-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="500fa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="500fa-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="500fa-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="500fa-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="500fa-135">INPUTS</span></span>

### <span data-ttu-id="500fa-136">Brak</span><span class="sxs-lookup"><span data-stu-id="500fa-136">None</span></span>

## <span data-ttu-id="500fa-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="500fa-137">OUTPUTS</span></span>

### <span data-ttu-id="500fa-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="500fa-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="500fa-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="500fa-139">NOTES</span></span>

## <span data-ttu-id="500fa-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="500fa-140">RELATED LINKS</span></span>
