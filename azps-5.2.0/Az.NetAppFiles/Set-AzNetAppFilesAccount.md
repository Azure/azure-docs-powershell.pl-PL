---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/set-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
ms.openlocfilehash: ecbf6a847ad208b49e11ab0089f9cf486763ddf3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364884"
---
# <span data-ttu-id="7f26d-101">Set-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="7f26d-101">Set-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="7f26d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7f26d-102">SYNOPSIS</span></span>
<span data-ttu-id="7f26d-103">Umożliwia zaktualizowanie konta usługi Azure NetApp Files (ANF) przy użyciu nowego zestawu danych.</span><span class="sxs-lookup"><span data-stu-id="7f26d-103">Updates an Azure NetApp Files (ANF) account with the new data set.</span></span> <span data-ttu-id="7f26d-104">Przydatne w przypadku usuwania skojarzonych z nimi aktywnych katalogów.</span><span class="sxs-lookup"><span data-stu-id="7f26d-104">Useful for deletion of associated active directories.</span></span>

## <span data-ttu-id="7f26d-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7f26d-105">SYNTAX</span></span>

### <span data-ttu-id="7f26d-106">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7f26d-106">ByFieldsParameterSet (Default)</span></span>
```
Set-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f26d-107">SetByResourceActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="7f26d-107">SetByResourceActiveDirectory</span></span>
```
Set-AzNetAppFilesAccount -Location <String> -Name <String> [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f26d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7f26d-108">DESCRIPTION</span></span>
<span data-ttu-id="7f26d-109">Polecenie cmdlet **Set-AzNetAppFilesAccount** modyfikuje konto usługi ANF.</span><span class="sxs-lookup"><span data-stu-id="7f26d-109">The **Set-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="7f26d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7f26d-110">EXAMPLES</span></span>

### <span data-ttu-id="7f26d-111">Przykład 1: modyfikowanie konta ANF</span><span class="sxs-lookup"><span data-stu-id="7f26d-111">Example 1 : Modify an ANF account</span></span>
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

<span data-ttu-id="7f26d-112">To polecenie wykonuje aktualizację na danym koncie.</span><span class="sxs-lookup"><span data-stu-id="7f26d-112">This command performs an update on the given account.</span></span> <span data-ttu-id="7f26d-113">Brak usługi Active Directory oznacza, że zostanie ona usunięta z konta.</span><span class="sxs-lookup"><span data-stu-id="7f26d-113">The absence of the active directory means it will be removed from the account.</span></span>

## <span data-ttu-id="7f26d-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7f26d-114">PARAMETERS</span></span>

### <span data-ttu-id="7f26d-115">-Pozycji</span><span class="sxs-lookup"><span data-stu-id="7f26d-115">-ActiveDirectory</span></span>
<span data-ttu-id="7f26d-116">Tablica Hashtable, która reprezentuje aktywne katalogi</span><span class="sxs-lookup"><span data-stu-id="7f26d-116">A hashtable array which represents the active directories</span></span>

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

### <span data-ttu-id="7f26d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f26d-117">-DefaultProfile</span></span>
<span data-ttu-id="7f26d-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7f26d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f26d-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="7f26d-119">-Location</span></span>
<span data-ttu-id="7f26d-120">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="7f26d-120">The location of the resource</span></span>

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

### <span data-ttu-id="7f26d-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7f26d-121">-Name</span></span>
<span data-ttu-id="7f26d-122">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="7f26d-122">The name of the ANF account</span></span>

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

### <span data-ttu-id="7f26d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f26d-123">-ResourceGroupName</span></span>
<span data-ttu-id="7f26d-124">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="7f26d-124">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="7f26d-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="7f26d-125">-Tag</span></span>
<span data-ttu-id="7f26d-126">Obiekt Hashtable reprezentujący znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="7f26d-126">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="7f26d-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7f26d-127">-Confirm</span></span>
<span data-ttu-id="7f26d-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f26d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f26d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f26d-129">-WhatIf</span></span>
<span data-ttu-id="7f26d-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f26d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f26d-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7f26d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f26d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f26d-132">CommonParameters</span></span>
<span data-ttu-id="7f26d-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f26d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f26d-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f26d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f26d-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7f26d-135">INPUTS</span></span>

### <span data-ttu-id="7f26d-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7f26d-136">None</span></span>

## <span data-ttu-id="7f26d-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7f26d-137">OUTPUTS</span></span>

### <span data-ttu-id="7f26d-138">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="7f26d-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="7f26d-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7f26d-139">NOTES</span></span>

## <span data-ttu-id="7f26d-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7f26d-140">RELATED LINKS</span></span>
