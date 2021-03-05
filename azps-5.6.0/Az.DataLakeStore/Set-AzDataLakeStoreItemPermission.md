---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 6ACE045E-67AD-40FE-86E4-450AF522F174
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/set-azdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemPermission.md
ms.openlocfilehash: 7294d5c48bd8cbc94ac127ac1f1543827dc2937b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995604"
---
# <span data-ttu-id="bb1de-101">Set-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="bb1de-101">Set-AzDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="bb1de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb1de-102">SYNOPSIS</span></span>
<span data-ttu-id="bb1de-103">Modyfikuje ósemkową ósemkową uprawnienia pliku lub folderu w sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="bb1de-103">Modifies the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="bb1de-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bb1de-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Permission] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb1de-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="bb1de-105">DESCRIPTION</span></span>
<span data-ttu-id="bb1de-106">Polecenie **cmdlet Set-AzDataLakeStoreItemPermission** modyfikuje ósemkową ósemkę uprawnień pliku lub folderu w magazynie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="bb1de-106">The **Set-AzDataLakeStoreItemPermission** cmdlet modifies the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="bb1de-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bb1de-107">EXAMPLES</span></span>

### <span data-ttu-id="bb1de-108">Przykład 1. Ustawianie ósemkowych uprawnień dla elementu</span><span class="sxs-lookup"><span data-stu-id="bb1de-108">Example 1: Set the permission octal for an item</span></span>
```
PS C:\>Set-AzDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt" -Permission 0770
```

<span data-ttu-id="bb1de-109">To polecenie ustawia dla pliku ósemkową uprawnienie na 0770, co przekłada się na wyczyszczenie bitu programu Sticky Bit, ustawienie uprawnień do odczytu/zapisu/wykonywania dla właściciela pliku, ustawienie uprawnień do odczytu/zapisu/wykonywania dla grupy, która jest właścicielem pliku, oraz wyczyszczenie uprawnień odczytu/zapisu/wykonywania dla innych.</span><span class="sxs-lookup"><span data-stu-id="bb1de-109">This command sets the permission octal for a file to 0770, which translates to clearing the sticky bit, setting read/write/execute permissions for the owner of the file, setting read/write/execute permissions for the owning group of the file, and clearing read/write/execute permissions for other.</span></span>

## <span data-ttu-id="bb1de-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb1de-110">PARAMETERS</span></span>

### <span data-ttu-id="bb1de-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="bb1de-111">-Account</span></span>
<span data-ttu-id="bb1de-112">Określa nazwę konta w sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="bb1de-112">Specifies the Data Lake Store account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb1de-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb1de-113">-DefaultProfile</span></span>
<span data-ttu-id="bb1de-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bb1de-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb1de-115">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="bb1de-115">-Path</span></span>
<span data-ttu-id="bb1de-116">Określa ścieżkę pliku lub folderu do magazynu Data Lake Store, zaczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="bb1de-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb1de-117">— Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="bb1de-117">-Permission</span></span>
<span data-ttu-id="bb1de-118">Uprawnienia do ustawienia pliku lub folderu wyrażone jako liczba ósemkowa (np. '777')</span><span class="sxs-lookup"><span data-stu-id="bb1de-118">The permissions to set for the file or folder, expressed as an octal (e.g. '777')</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb1de-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bb1de-119">-Confirm</span></span>
<span data-ttu-id="bb1de-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bb1de-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb1de-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb1de-121">-WhatIf</span></span>
<span data-ttu-id="bb1de-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb1de-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb1de-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bb1de-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb1de-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb1de-124">CommonParameters</span></span>
<span data-ttu-id="bb1de-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb1de-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb1de-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb1de-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb1de-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb1de-127">INPUTS</span></span>

### <span data-ttu-id="bb1de-128">System.String</span><span class="sxs-lookup"><span data-stu-id="bb1de-128">System.String</span></span>

### <span data-ttu-id="bb1de-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="bb1de-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="bb1de-130">System.Int32</span><span class="sxs-lookup"><span data-stu-id="bb1de-130">System.Int32</span></span>

## <span data-ttu-id="bb1de-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb1de-131">OUTPUTS</span></span>

### <span data-ttu-id="bb1de-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bb1de-132">System.Boolean</span></span>

## <span data-ttu-id="bb1de-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bb1de-133">NOTES</span></span>
* <span data-ttu-id="bb1de-134">Alias: Set-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="bb1de-134">Alias: Set-AdlStoreItemPermission</span></span>

## <span data-ttu-id="bb1de-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bb1de-135">RELATED LINKS</span></span>

[<span data-ttu-id="bb1de-136">Get-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="bb1de-136">Get-AzDataLakeStoreItemPermission</span></span>](./Get-AzDataLakeStoreItemPermission.md)


