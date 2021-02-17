---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D077DB50-12BC-45AB-8EAC-57810DA83035
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchremotedesktopprotocolfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteDesktopProtocolFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteDesktopProtocolFile.md
ms.openlocfilehash: 3e1b4ce662e7a904fcfb8d4b938f7fe5bbef0f7e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197099"
---
# <span data-ttu-id="51e01-101">Get-AzBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="51e01-101">Get-AzBatchRemoteDesktopProtocolFile</span></span>

## <span data-ttu-id="51e01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51e01-102">SYNOPSIS</span></span>
<span data-ttu-id="51e01-103">Pobiera plik RDP z węzła obliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="51e01-103">Gets an RDP file from a compute node.</span></span>

## <span data-ttu-id="51e01-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="51e01-104">SYNTAX</span></span>

### <span data-ttu-id="51e01-105">Id_Path (domyślne)</span><span class="sxs-lookup"><span data-stu-id="51e01-105">Id_Path (Default)</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51e01-106">Id_Stream</span><span class="sxs-lookup"><span data-stu-id="51e01-106">Id_Stream</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51e01-107">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="51e01-107">InputObject_Path</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51e01-108">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="51e01-108">InputObject_Stream</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51e01-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="51e01-109">DESCRIPTION</span></span>
<span data-ttu-id="51e01-110">Polecenie **cmdlet Get-AzBatchRemoteDesktopProtocolFile** pobiera plik protokołu RDP (Remote Desktop Protocol) z węzła obliczeniowego i zapisuje go jako plik lub w strumieniu dostarczonym przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="51e01-110">The **Get-AzBatchRemoteDesktopProtocolFile** cmdlet gets a Remote Desktop Protocol (RDP) file from a compute node and saves it as a file or to a user supplied stream.</span></span>

## <span data-ttu-id="51e01-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="51e01-111">EXAMPLES</span></span>

### <span data-ttu-id="51e01-112">Przykład 1. Uzyskiwanie pliku RDP z określonego węzła obliczeniowego i zapisywanie pliku</span><span class="sxs-lookup"><span data-stu-id="51e01-112">Example 1: Get an RDP file from a specified compute node and save the file</span></span>
```
PS C:\>Get-AzBatchRemoteDesktopProtocolFile -PoolId "Pool06" -ComputeNodeId "ComputeNode01" -DestinationPath "C:\PowerShell\ComputeNode01.rdp" -BatchContext $Context
```

<span data-ttu-id="51e01-113">To polecenie pobiera plik RDP z węzła obliczeniowego, który ma identyfikator ComputeNode01 w puli, która ma pulę identyfikatorów 06.</span><span class="sxs-lookup"><span data-stu-id="51e01-113">This command gets an RDP file from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="51e01-114">Polecenie zapisuje plik rdp w następujący sposób: C:\PowerShell\MyComputeNode.rdp.</span><span class="sxs-lookup"><span data-stu-id="51e01-114">The command saves the .rdp file as C:\PowerShell\MyComputeNode.rdp.</span></span>
<span data-ttu-id="51e01-115">Użyj Get-AzBatchAccountKey cmdlet, aby przypisać kontekst do zmiennej $Context danych.</span><span class="sxs-lookup"><span data-stu-id="51e01-115">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="51e01-116">Przykład 2. Pobierz plik RDP z węzła obliczeniowego i zapisz plik przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="51e01-116">Example 2: Get an RDP file from a compute node and save the file by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool06" -Id "ComputeNode02" -BatchContext $Context | Get-AzBatchRemoteDesktopProtocolFile -DestinationPath "C:\PowerShell\MyComputeNode02.rdp" -BatchContext $Context
```

<span data-ttu-id="51e01-117">To polecenie pobiera węzeł obliczeniowy o identyfikatorze ComputeNode02 w puli, która ma pulę identyfikatorów 06.</span><span class="sxs-lookup"><span data-stu-id="51e01-117">This command gets the compute node that has the ID ComputeNode02 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="51e01-118">Polecenie przekazuje węzeł obliczeniowy do bieżącego polecenia cmdlet przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="51e01-118">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="51e01-119">Bieżące polecenie cmdlet pobiera plik csv z węzła obliczeniowego, a następnie zapisuje zawartość jako plik o nazwie C:\PowerShell\MyComputeNode02.rdp.</span><span class="sxs-lookup"><span data-stu-id="51e01-119">The current cmdlet gets an .rpd file from the compute node, and then saves the contents as a file that is named C:\PowerShell\MyComputeNode02.rdp.</span></span>

### <span data-ttu-id="51e01-120">Przykład 3. Pobierz plik RDP z określonego węzła obliczeniowego i przekieruj go do strumienia</span><span class="sxs-lookup"><span data-stu-id="51e01-120">Example 3: Get a RDP file from a specified compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchRemoteDesktopProtocolFile "Pool06" -ComputeNodeId "ComputeNode03" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="51e01-121">Pierwsze polecenie tworzy strumień przy użyciu New-Object cmdlet, a następnie zapisuje go w $Stream zmienną.</span><span class="sxs-lookup"><span data-stu-id="51e01-121">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="51e01-122">Drugie polecenie pobiera plik rdp z węzła obliczeniowego, który ma identyfikator ComputeNode03 w puli, która ma pulę identyfikatorów 06.</span><span class="sxs-lookup"><span data-stu-id="51e01-122">The second command gets an .rdp file from the compute node that has the ID ComputeNode03 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="51e01-123">Polecenie kieruje zawartość pliku do strumienia w $Stream.</span><span class="sxs-lookup"><span data-stu-id="51e01-123">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="51e01-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51e01-124">PARAMETERS</span></span>

### <span data-ttu-id="51e01-125">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="51e01-125">-BatchContext</span></span>
<span data-ttu-id="51e01-126">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="51e01-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="51e01-127">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="51e01-127">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="51e01-128">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="51e01-128">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="51e01-129">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="51e01-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="51e01-130">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="51e01-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51e01-131">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="51e01-131">-ComputeNode</span></span>
<span data-ttu-id="51e01-132">Określa węzeł obliczeniowy jako **obiekt PSComputeNode,** do którego punkty pliku rdp.</span><span class="sxs-lookup"><span data-stu-id="51e01-132">Specifies a compute node, as a **PSComputeNode** object, to which the .rdp file points.</span></span>
<span data-ttu-id="51e01-133">Aby uzyskać obiekt węzła obliczeniowego, użyj Get-AzBatchComputeNode cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51e01-133">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject_Path, InputObject_Stream
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51e01-134">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="51e01-134">-ComputeNodeId</span></span>
<span data-ttu-id="51e01-135">Określa identyfikator węzła obliczeniowego, do którego mają być punktami pliku rdp.</span><span class="sxs-lookup"><span data-stu-id="51e01-135">Specifies the ID of the compute node to which the .rdp file points.</span></span>

```yaml
Type: System.String
Parameter Sets: Id_Path, Id_Stream
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51e01-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51e01-136">-DefaultProfile</span></span>
<span data-ttu-id="51e01-137">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="51e01-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51e01-138">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="51e01-138">-DestinationPath</span></span>
<span data-ttu-id="51e01-139">Określa ścieżkę pliku, w której to polecenie cmdlet zapisuje plik rdp.</span><span class="sxs-lookup"><span data-stu-id="51e01-139">Specifies the file path where this cmdlet saves the .rdp file.</span></span>

```yaml
Type: System.String
Parameter Sets: Id_Path, InputObject_Path
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e01-140">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="51e01-140">-DestinationStream</span></span>
<span data-ttu-id="51e01-141">Określa strumień, do którego to polecenie cmdlet kieruje danymi RDP.</span><span class="sxs-lookup"><span data-stu-id="51e01-141">Specifies the stream into which this cmdlet directs the RDP data.</span></span>
<span data-ttu-id="51e01-142">To polecenie cmdlet nie zamyka ani nie przewija tego strumienia.</span><span class="sxs-lookup"><span data-stu-id="51e01-142">This cmdlet does not close or rewind this stream.</span></span>

```yaml
Type: System.IO.Stream
Parameter Sets: Id_Stream, InputObject_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e01-143">- PoolId</span><span class="sxs-lookup"><span data-stu-id="51e01-143">-PoolId</span></span>
<span data-ttu-id="51e01-144">Określa identyfikator puli zawierającej węzeł obliczeniowy, z którego to polecenie cmdlet pobiera plik rdp.</span><span class="sxs-lookup"><span data-stu-id="51e01-144">Specifies the ID of the pool that contains the compute node from which this cmdlet gets an .rdp file.</span></span>

```yaml
Type: System.String
Parameter Sets: Id_Path, Id_Stream
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51e01-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51e01-145">CommonParameters</span></span>
<span data-ttu-id="51e01-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51e01-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51e01-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="51e01-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51e01-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="51e01-148">INPUTS</span></span>

### <span data-ttu-id="51e01-149">System.String</span><span class="sxs-lookup"><span data-stu-id="51e01-149">System.String</span></span>

### <span data-ttu-id="51e01-150">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="51e01-150">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="51e01-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="51e01-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="51e01-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="51e01-152">OUTPUTS</span></span>

### <span data-ttu-id="51e01-153">System.Void</span><span class="sxs-lookup"><span data-stu-id="51e01-153">System.Void</span></span>

## <span data-ttu-id="51e01-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="51e01-154">NOTES</span></span>

## <span data-ttu-id="51e01-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="51e01-155">RELATED LINKS</span></span>

[<span data-ttu-id="51e01-156">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="51e01-156">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="51e01-157">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="51e01-157">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="51e01-158">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="51e01-158">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
