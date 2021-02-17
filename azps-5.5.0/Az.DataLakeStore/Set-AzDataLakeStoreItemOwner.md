---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 415C5854-FE03-4D4E-BE84-408EA5F95E34
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemOwner.md
ms.openlocfilehash: fc7c0e7ff8ef86b4a33f93e6b1286bb6e0baa00d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194626"
---
# <span data-ttu-id="c9eae-101">Set-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="c9eae-101">Set-AzDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="c9eae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9eae-102">SYNOPSIS</span></span>
<span data-ttu-id="c9eae-103">Modyfikuje właściciela pliku lub folderu w sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c9eae-103">Modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="c9eae-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c9eae-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-Id] <Guid> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9eae-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c9eae-105">DESCRIPTION</span></span>
<span data-ttu-id="c9eae-106">Polecenie cmdlet **Set-AzDataLakeStoreItemOwner** modyfikuje właściciela pliku lub folderu w magazynie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c9eae-106">The **Set-AzDataLakeStoreItemOwner** cmdlet modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="c9eae-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c9eae-107">EXAMPLES</span></span>

### <span data-ttu-id="c9eae-108">Przykład 1. Ustawianie właściciela elementu</span><span class="sxs-lookup"><span data-stu-id="c9eae-108">Example 1: Set the owner for an item</span></span>
```
PS C:\>Set-AzDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="c9eae-109">To polecenie ustawia właściciela katalogu głównego na Patti Fuller.</span><span class="sxs-lookup"><span data-stu-id="c9eae-109">This command sets the owner for the root directory to Patti Fuller.</span></span>

## <span data-ttu-id="c9eae-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9eae-110">PARAMETERS</span></span>

### <span data-ttu-id="c9eae-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="c9eae-111">-Account</span></span>
<span data-ttu-id="c9eae-112">Określa nazwę konta sklepu Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c9eae-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="c9eae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9eae-113">-DefaultProfile</span></span>
<span data-ttu-id="c9eae-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c9eae-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9eae-115">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="c9eae-115">-Id</span></span>
<span data-ttu-id="c9eae-116">Określa identyfikator obiektu użytkownika, grupy lub podmiotu zabezpieczeń usługi AzureActive Directory, który ma być właścicielem.</span><span class="sxs-lookup"><span data-stu-id="c9eae-116">Specifies the object ID of the AzureActive Directory user, group, or service principal to use as the owner.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9eae-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c9eae-117">-PassThru</span></span>
<span data-ttu-id="c9eae-118">Wskazuje, że wynikowa aktualizacja właściciela powinna zostać zwrócona.</span><span class="sxs-lookup"><span data-stu-id="c9eae-118">Indicates the resulting updated owner should be returned.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9eae-119">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="c9eae-119">-Path</span></span>
<span data-ttu-id="c9eae-120">Określa ścieżkę elementu do zmodyfikowania w sklepie Data Lake Store, zaczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="c9eae-120">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="c9eae-121">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="c9eae-121">-Type</span></span>
<span data-ttu-id="c9eae-122">Określa typ właściciela, który ma być ustawiany.</span><span class="sxs-lookup"><span data-stu-id="c9eae-122">Specifies the type of owner to set.</span></span>
<span data-ttu-id="c9eae-123">Dopuszczalne wartości dla tego parametru to: Użytkownik i Grupa.</span><span class="sxs-lookup"><span data-stu-id="c9eae-123">The acceptable values for this parameter are: User and Group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner
Parameter Sets: (All)
Aliases:
Accepted values: User, Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9eae-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c9eae-124">-Confirm</span></span>
<span data-ttu-id="c9eae-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c9eae-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9eae-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9eae-126">-WhatIf</span></span>
<span data-ttu-id="c9eae-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9eae-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9eae-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c9eae-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9eae-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9eae-129">CommonParameters</span></span>
<span data-ttu-id="c9eae-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9eae-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9eae-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9eae-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9eae-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9eae-132">INPUTS</span></span>

### <span data-ttu-id="c9eae-133">System.String</span><span class="sxs-lookup"><span data-stu-id="c9eae-133">System.String</span></span>

### <span data-ttu-id="c9eae-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="c9eae-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="c9eae-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Właściciel</span><span class="sxs-lookup"><span data-stu-id="c9eae-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

### <span data-ttu-id="c9eae-136">System.Guid</span><span class="sxs-lookup"><span data-stu-id="c9eae-136">System.Guid</span></span>

### <span data-ttu-id="c9eae-137">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="c9eae-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c9eae-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c9eae-138">OUTPUTS</span></span>

### <span data-ttu-id="c9eae-139">System.String</span><span class="sxs-lookup"><span data-stu-id="c9eae-139">System.String</span></span>

## <span data-ttu-id="c9eae-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c9eae-140">NOTES</span></span>

## <span data-ttu-id="c9eae-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c9eae-141">RELATED LINKS</span></span>

[<span data-ttu-id="c9eae-142">Get-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="c9eae-142">Get-AzDataLakeStoreItemOwner</span></span>](./Get-AzDataLakeStoreItemOwner.md)


