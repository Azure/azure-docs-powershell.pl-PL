---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
ms.openlocfilehash: 525483bdb99867ae9403c95a6bc2dc83a855704a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380494"
---
# <span data-ttu-id="5c192-101">Update-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="5c192-101">Update-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="5c192-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5c192-102">SYNOPSIS</span></span>
<span data-ttu-id="5c192-103">Umożliwia zaktualizowanie konta usługi Azure NetApp (ANF) zgodnie z podanym opcjonalnymi modyfikatorami.</span><span class="sxs-lookup"><span data-stu-id="5c192-103">Updates an Azure NetApp Files (ANF) account according to the optional modifiers provided.</span></span>

## <span data-ttu-id="5c192-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5c192-104">SYNTAX</span></span>

### <span data-ttu-id="5c192-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5c192-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c192-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c192-106">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 -ResourceId <String> [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c192-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c192-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] -InputObject <PSNetAppFilesAccount> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c192-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5c192-108">DESCRIPTION</span></span>
<span data-ttu-id="5c192-109">Polecenie cmdlet **Update-AzNetAppFilesAccount** modyfikuje konto usługi ANF.</span><span class="sxs-lookup"><span data-stu-id="5c192-109">The **Update-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="5c192-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5c192-110">EXAMPLES</span></span>

### <span data-ttu-id="5c192-111">Przykład 1: aktualizowanie konta programu ANF</span><span class="sxs-lookup"><span data-stu-id="5c192-111">Example 1 : Updates an ANF account</span></span>
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

<span data-ttu-id="5c192-112">To polecenie wykonuje aktualizację na danym koncie, modyfikując odpowiednie znaczniki.</span><span class="sxs-lookup"><span data-stu-id="5c192-112">This command performs an update on the given account modifying the tags to those provided.</span></span>

## <span data-ttu-id="5c192-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5c192-113">PARAMETERS</span></span>

### <span data-ttu-id="5c192-114">-Pozycji</span><span class="sxs-lookup"><span data-stu-id="5c192-114">-ActiveDirectory</span></span>
<span data-ttu-id="5c192-115">Tablica Hashtable, która reprezentuje aktywne katalogi</span><span class="sxs-lookup"><span data-stu-id="5c192-115">A hashtable array which represents the active directories</span></span>

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

### <span data-ttu-id="5c192-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c192-116">-DefaultProfile</span></span>
<span data-ttu-id="5c192-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5c192-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c192-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5c192-118">-InputObject</span></span>
<span data-ttu-id="5c192-119">Obiekt konta do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="5c192-119">The account object to update</span></span>

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

### <span data-ttu-id="5c192-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5c192-120">-Location</span></span>
<span data-ttu-id="5c192-121">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="5c192-121">The location of the resource</span></span>

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

### <span data-ttu-id="5c192-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5c192-122">-Name</span></span>
<span data-ttu-id="5c192-123">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="5c192-123">The name of the ANF account</span></span>

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

### <span data-ttu-id="5c192-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c192-124">-ResourceGroupName</span></span>
<span data-ttu-id="5c192-125">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="5c192-125">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="5c192-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c192-126">-ResourceId</span></span>
<span data-ttu-id="5c192-127">Identyfikator zasobu konta ANF</span><span class="sxs-lookup"><span data-stu-id="5c192-127">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="5c192-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="5c192-128">-Tag</span></span>
<span data-ttu-id="5c192-129">Obiekt Hashtable reprezentujący znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="5c192-129">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="5c192-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5c192-130">-Confirm</span></span>
<span data-ttu-id="5c192-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c192-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c192-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c192-132">-WhatIf</span></span>
<span data-ttu-id="5c192-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c192-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c192-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5c192-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c192-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c192-135">CommonParameters</span></span>
<span data-ttu-id="5c192-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c192-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c192-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5c192-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c192-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5c192-138">INPUTS</span></span>

### <span data-ttu-id="5c192-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5c192-139">System.String</span></span>

### <span data-ttu-id="5c192-140">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="5c192-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="5c192-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5c192-141">OUTPUTS</span></span>

### <span data-ttu-id="5c192-142">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="5c192-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="5c192-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5c192-143">NOTES</span></span>

## <span data-ttu-id="5c192-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5c192-144">RELATED LINKS</span></span>
