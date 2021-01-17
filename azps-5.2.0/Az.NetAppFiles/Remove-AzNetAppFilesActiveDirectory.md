---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 7fcf1f749816872fb7407fedaea10d06f3385441
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359863"
---
# <span data-ttu-id="e64e1-101">Remove-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="e64e1-101">Remove-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="e64e1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e64e1-102">SYNOPSIS</span></span>
<span data-ttu-id="e64e1-103">Usuwa konfigurację usługi Active Directory usługi Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="e64e1-103">Deletes an Azure NetApp Files (ANF) active directory configuration.</span></span>

## <span data-ttu-id="e64e1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e64e1-104">SYNTAX</span></span>

### <span data-ttu-id="e64e1-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e64e1-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String>
 -ActiveDirectoryId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e64e1-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e64e1-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesActiveDirectory -ActiveDirectoryId <String> -AccountObject <PSNetAppFilesAccount>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e64e1-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e64e1-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesActiveDirectory -InputObject <PSNetAppFilesActiveDirectory> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e64e1-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e64e1-108">DESCRIPTION</span></span>
<span data-ttu-id="e64e1-109">Polecenie cmdlet **Remove-AzNetAppFilesActiveDirectory** usuwa konfigurację usługi ANF Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e64e1-109">The **Remove-AzNetAppFilesActiveDirectory** cmdlet deletes an ANF active directory configuration.</span></span>

## <span data-ttu-id="e64e1-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e64e1-110">EXAMPLES</span></span>

### <span data-ttu-id="e64e1-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e64e1-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesActiveDirectory -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyADName"
```

<span data-ttu-id="e64e1-112">To polecenie usuwa nową konfigurację usługi ANF Active Directory o nazwie "MyADName".</span><span class="sxs-lookup"><span data-stu-id="e64e1-112">This command deletes the new ANF active directory configuration with a the name "MyADName".</span></span>

## <span data-ttu-id="e64e1-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e64e1-113">PARAMETERS</span></span>

### <span data-ttu-id="e64e1-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e64e1-114">-AccountName</span></span>
<span data-ttu-id="e64e1-115">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="e64e1-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="e64e1-116">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="e64e1-116">-AccountObject</span></span>
<span data-ttu-id="e64e1-117">Konto obiektu usługi Active Directory</span><span class="sxs-lookup"><span data-stu-id="e64e1-117">The Account for the Active Directory object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e64e1-118">-ActiveDirectoryId</span><span class="sxs-lookup"><span data-stu-id="e64e1-118">-ActiveDirectoryId</span></span>
<span data-ttu-id="e64e1-119">Identyfikator usługi ANF Active Directory</span><span class="sxs-lookup"><span data-stu-id="e64e1-119">The ID of the ANF active directory</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e64e1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e64e1-120">-DefaultProfile</span></span>
<span data-ttu-id="e64e1-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e64e1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e64e1-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e64e1-122">-InputObject</span></span>
<span data-ttu-id="e64e1-123">Obiekt usługi Active Directory do usunięcia</span><span class="sxs-lookup"><span data-stu-id="e64e1-123">The active directory object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e64e1-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e64e1-124">-PassThru</span></span>
<span data-ttu-id="e64e1-125">Zwracanie, czy określona usługa Active Directory została pomyślnie usunięta</span><span class="sxs-lookup"><span data-stu-id="e64e1-125">Return whether the specified Active Directory  was successfully removed</span></span>

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

### <span data-ttu-id="e64e1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e64e1-126">-ResourceGroupName</span></span>
<span data-ttu-id="e64e1-127">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="e64e1-127">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="e64e1-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e64e1-128">-Confirm</span></span>
<span data-ttu-id="e64e1-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e64e1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e64e1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e64e1-130">-WhatIf</span></span>
<span data-ttu-id="e64e1-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e64e1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e64e1-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e64e1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e64e1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e64e1-133">CommonParameters</span></span>
<span data-ttu-id="e64e1-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e64e1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e64e1-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e64e1-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e64e1-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e64e1-136">INPUTS</span></span>

### <span data-ttu-id="e64e1-137">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="e64e1-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="e64e1-138">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="e64e1-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="e64e1-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e64e1-139">OUTPUTS</span></span>

### <span data-ttu-id="e64e1-140">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="e64e1-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="e64e1-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e64e1-141">NOTES</span></span>

## <span data-ttu-id="e64e1-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e64e1-142">RELATED LINKS</span></span>
